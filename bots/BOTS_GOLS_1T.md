# Bots de Gols no Primeiro Tempo — Pacote Novo

Documento de configuração para criar bots novos no painel SokkerPRO (https://go.sokkerpro.com).
Todos os campos abaixo existem no manual `sokkerprobots.pdf` — nenhum campo foi inventado.

---

## 1. Análise: por que bots de 1T ficam negativos

Lendo as definições de mercado do manual (Passo 1), existe uma assimetria enorme
entre os quatro mercados de gols do primeiro tempo:

| Mercado | 0 gols | 1 gol | 2+ gols | Dificuldade |
|---|---|---|---|---|
| Mais um gol até o fim do 1T | Perde | **Ganha** | Ganha | Fácil |
| Mais um gol **asiático** até o fim do 1T | Perde | *Devolve* | **Ganha** | **Muito difícil** |
| Sem mais gols até o fim do 1T | **Ganha** | Perde | Perde | Média |
| Sem mais gols **(asiático)** até o fim do 1T | **Ganha** | *Devolve* | Perde | **Mais seguro** |

**Causa nº 1 de bot negativo:** usar *"Mais um gol asiático"* como se fosse uma
proteção. Ele **não** protege — ele exige **2 gols** antes do intervalo para pagar.
Sair 2 gols entre o minuto ~25 e o intervalo é um evento raro. Se algum bot negativo
usa esse mercado com janela de minutos alta, é matematicamente esperado que ele perca.

**Causa nº 2:** janela de minutos curta demais para o mercado escolhido. Entrar em
"mais um gol" no minuto 38 deixa ~7 minutos + acréscimos para o gol sair.

**Causa nº 3:** condições exigentes demais → o bot não gera entradas, ou só entra
em jogos já esticados (odd baixa, sem valor).

**Consequência de projeto deste pacote:**
- O mercado protegido *"Sem mais gols (asiático)"* é priorizado nos bots de under.
- O mercado *"Mais um gol asiático"* aparece **uma única vez**, e com janela bem
  cedo (minuto 8–22) para ter tempo real de sair 2 gols. É o bot de maior variância
  do pacote — marcado como tal.

---

## 2. Calibragem para garantir entradas

As estatísticas ao vivo são **acumulativas** (só sobem durante o jogo). Referência de
mediana aproximada, somando os dois times:

| Estatística (Ambos Somados) | ~min 25 | ~min 30 | ~min 38 |
|---|---|---|---|
| Ataques Totais | 38 | 48 | 60 |
| Ataques Perigosos | 22 | 30 | 38 |
| Total de Chutes | 6 | 9 | 11 |
| Chutes no Gol | 2 | 3 | 4 |
| Escanteios | 3 | 4 | 5 |

Os limiares dos bots de **over** foram postos **na mediana ou levemente acima** —
selecionam o jogo movimentado sem zerar o volume de alertas. Os bots de **under**
usam **tetos** bem abaixo da mediana, porque jogo morto é minoria.

---

## 3. Os bots

> **Valor de Entrada:** preencha com seu stake fixo em todos. Sem valor preenchido o
> bot só alerta e **não contabiliza lucro/ROI** (manual, Passo 2) — e você não
> conseguiria avaliar o desempenho amanhã.
>
> **Contador:** todo bot criado do zero já nasce com contador zerado. Basta criar
> estes como bots **novos** e arquivar/apagar os negativos — não reaproveite o bot
> antigo editando, senão o histórico ruim continua somando.

---

### SP-1T-01 · Pressão Sustentada
Jogo de volume alto que ainda não converteu. O mais estável do pacote.

- **Mercado:** Mais um gol até o fim do primeiro tempo
- **Faixa de minutos:** De `26` até `38`
- **Odd mínima:** `1.60`
- **Filtro de placar:** Qualquer

**Condições PRÉ-JOGO**
- Prognóstico Over 0.5 (1T) `≥ 60`
- Média de Gols (1T) `≥ 1.0`

**Condições AO VIVO**
- Ambos Somados · Ataques Perigosos `≥ 28`
- Ambos Somados · Chutes no Gol `≥ 4`
- Ambos Somados · Escanteios `≥ 4`

**Ligas:** Pacote A (over)

---

### SP-1T-02 · Favorito Travado
Favorito dominando e sem marcar. O gol costuma sair por acúmulo de chance clara.
Assinatura totalmente diferente do 01 — usa Favorito/Zebra em vez de soma.

- **Mercado:** Mais um gol até o fim do primeiro tempo
- **Faixa de minutos:** De `24` até `40`
- **Odd mínima:** `1.55`
- **Filtro de placar:** Favorito perdendo ou empatando

**Condições PRÉ-JOGO**
- Prognóstico Over 0.5 (1T) `≥ 56`

**Condições AO VIVO**
- Favorito · Chutes Dentro da Área `≥ 4`
- Favorito · Chutes no Gol `≥ 3`
- Favorito · Ataques Perigosos `≥ 16`
- Zebra · Defesas do Goleiro `≥ 3`

> A condição do goleiro da zebra é o filtro-chave: pelo manual, "defesas do goleiro
> indica pressão sofrida". 3+ defesas = o favorito está criando chance real, não só
> tocando a bola.

**Ligas:** Pacote A (over)

---

### SP-1T-03 · Início Elétrico
Entra cedo, quando ainda há muito tempo de primeiro tempo pela frente.
Usa as médias curtas (3/5 min), que nenhum outro bot do pacote usa.

- **Mercado:** Mais um gol até o fim do primeiro tempo
- **Faixa de minutos:** De `10` até `25`
- **Odd mínima:** `1.40`
- **Filtro de placar:** Qualquer

**Condições PRÉ-JOGO**
- Prognóstico Over 0.5 (1T) `≥ 58`
- Média de Ataques Perigosos (1T) `≥ 22`

**Condições AO VIVO**
- Ambos Somados · Ataques Perigosos `≥ 14`
- Qualquer Time · Ataques perigosos 5 minutos `≥ 1.3`
- Qualquer Time · Barra de Pressão `≥ 65`

**Ligas:** Pacote A (over)

---

### SP-1T-04 · Jogo Aberto Asiático ⚠️ alta variância
Único bot do pacote no mercado asiático de over. Exige **2 gols**, por isso a janela
é a mais cedo de todas e os filtros pré-jogo são os mais duros.

- **Mercado:** Mais um gol asiático até o fim do primeiro tempo
- **Faixa de minutos:** De `8` até `22`
- **Odd mínima:** `1.80`
- **Filtro de placar:** Qualquer

**Condições PRÉ-JOGO**
- Prognóstico Over 1.5 (1T) `≥ 45`
- Média de Gols (1T) `≥ 1.4`
- Prognóstico Ambas Marcam (Sim) `≥ 62`

**Condições AO VIVO**
- Ambos Somados · Ataques Perigosos `≥ 12`
- Ambos Somados · Total de Chutes `≥ 5`

> Rode com **stake reduzido** (metade do padrão) no teste. Se após ~30 entradas ele
> não estiver no positivo, é o primeiro candidato a ser desligado.

**Ligas:** Pacote A (over) — apenas as de maior média de gols

---

### SP-1T-05 · Blindado Asiático
Mercado mais seguro da tabela: 1 gol apenas devolve o stake. Entra tarde, em jogo
de ritmo baixo.

- **Mercado:** Sem mais gols (asiático) até o fim do primeiro tempo
- **Faixa de minutos:** De `30` até `43`
- **Odd mínima:** `1.35`
- **Filtro de placar:** Qualquer

**Condições PRÉ-JOGO**
- Prognóstico Over 0.5 (1T) `≤ 50`
- Média de Gols (1T) `≤ 0.9`

**Condições AO VIVO** *(tetos — ver nota de operação)*
- Ambos Somados · Ataques Perigosos `≤ 26`
- Ambos Somados · Chutes no Gol `≤ 3`
- Ambos Somados · Total de Chutes `≤ 8`

**Ligas:** Pacote B (under)

---

### SP-1T-06 · Zero a Zero Travado
O clássico jogo morto, entrando bem no fim do primeiro tempo. Mercado sem proteção,
por isso os filtros são os mais restritivos e a janela a mais curta.

- **Mercado:** Sem mais gols até o fim do primeiro tempo
- **Faixa de minutos:** De `34` até `44`
- **Odd mínima:** `1.15`
- **Filtro de placar:** Empate

**Condições PRÉ-JOGO**
- Prognóstico Over 0.5 (1T) `≤ 48`
- Média de Gols (1T) `≤ 0.85`

**Condições AO VIVO** *(tetos)*
- Ambos Somados · Ataques Perigosos `≤ 24`
- Ambos Somados · Chutes no Gol `≤ 2`
- Ambos Somados · Escanteios `≤ 4`
- Qualquer Time · Barra de Pressão `≤ 66`

**Ligas:** Pacote B (under)

---

## 4. Seleção de campeonatos

⚠️ **Como o filtro funciona:** pelo manual (última página), o filtro de ligas é por
**remoção** — "você pode remover ligas para que o bot não alerte nelas". Não existe
lista de inclusão. Para deixar só as ligas abaixo, é preciso **remover todo o resto**
em cada bot.

### Pacote A — bots de OVER (SP-1T-01, 02, 03, 04)
Ligas de alta média de gols no 1T e com estatística ao vivo confiável.

| País | Liga |
|---|---|
| Holanda | Eredivisie |
| Holanda | Eerste Divisie |
| Alemanha | Bundesliga |
| Alemanha | 2. Bundesliga |
| Alemanha | 3. Liga |
| Áustria | Bundesliga |
| Suíça | Super League |
| Bélgica | Pro League |
| Dinamarca | Superliga |
| Noruega | Eliteserien |
| Suécia | Allsvenskan |
| Inglaterra | Premier League |
| Inglaterra | Championship |
| Escócia | Premiership |
| EUA | MLS |
| Japão | J1 League |
| Coreia do Sul | K League 1 |

Para o **SP-1T-04** (asiático), reduza a: Eredivisie, Eerste Divisie, Bundesliga,
2. Bundesliga, Áustria Bundesliga, Suíça Super League, MLS.

### Pacote B — bots de UNDER (SP-1T-05, 06)
Ligas historicamente travadas no primeiro tempo.

| País | Liga |
|---|---|
| Argentina | Liga Profesional |
| Brasil | Série B |
| Itália | Serie B |
| Espanha | LaLiga Hypermotion (2ª div.) |
| França | Ligue 2 |
| Portugal | Liga Portugal 2 |
| Grécia | Super League 1 |
| Turquia | 1. Lig |
| Colômbia | Primera A |
| Chile | Primera División |

**Nota de calendário (agosto):** as ligas europeias estão nas primeiras rodadas —
as médias H2H usam os últimos 5 jogos (manual, Passo 3), então nas 5 primeiras
rodadas elas ainda carregam jogos da temporada passada. MLS, Escandinávia, Japão,
Coreia e América do Sul estão em meio de temporada e são as fontes mais confiáveis
de entrada agora.

---

## 5. Nota de operação — condições de teto

Os bots 05 e 06 dependem de **valores máximos** (jogo abaixo de X). Se o painel
oferecer campo de faixa (mínimo/máximo) por condição, use o campo de máximo.
Se a condição só aceitar valor mínimo, esses dois bots não são configuráveis como
descritos — nesse caso me avise que eu reescrevo o 05 e o 06 usando apenas
prognósticos pré-jogo baixos + filtro de placar, que são filtros de inclusão.

---

## 6. Checklist antes de ligar

- [ ] Criar os 6 como bots **novos** (contador nasce zerado)
- [ ] Arquivar/apagar os bots negativos que estes substituem
- [ ] Preencher **Valor de Entrada** em todos (senão não há ROI para avaliar)
- [ ] Aplicar a remoção de ligas em cada bot
- [ ] Conferir que nenhum destes duplica um bot já existente
