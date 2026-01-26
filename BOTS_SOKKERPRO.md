# 🤖 8 BOTS SOKKERPRO - Configuração Completa

Este documento contém 8 bots estratégicos e bem elaborados para o SokkerPro, divididos em 4 categorias com 2 bots cada. As condições foram calibradas para se enquadrarem em partidas reais, evitando filtros muito restritivos.

---

## 📋 PASSO A PASSO PARA ADICIONAR OS BOTS

### Como Adicionar um Bot no SokkerPro:

1. **Acesse o painel de bots**: Vá em https://go.sokkerpro.com e faça login
2. **Clique em "Criar Novo Bot"** ou "Adicionar Bot"
3. **Passo 1 - Informações Básicas**: Selecione o mercado (Gols, Escanteios, Resultado)
4. **Passo 2 - Configuração Essencial**: Configure a faixa de minutos, odd mínima, valor de entrada e filtro de placar
5. **Passo 3 - Condições**: Adicione as condições ao vivo e pré-jogo conforme especificado em cada bot
6. **Salve o bot** e monitore os alertas

### Dicas Importantes:
- Comece com valores baixos para testar
- Monitore o ROI dos primeiros 50 alertas antes de aumentar as stakes
- Ajuste as condições conforme necessário baseado nos resultados

---

## ⚽ CATEGORIA 1: BOTS DE GOLS NO PRIMEIRO TEMPO (2 Bots)

### 🎯 BOT 1: "Pressão Total 1T - Over 0.5"

**Conceito**: Identifica jogos com alta pressão ofensiva onde pelo menos 1 gol é esperado no primeiro tempo.

#### Passo 1 - Informações Básicas:
| Campo | Valor |
|-------|-------|
| **Mercado** | Mais um gol até o fim do primeiro tempo |

#### Passo 2 - Configuração Essencial:
| Campo | Valor |
|-------|-------|
| **De (minuto)** | 15 |
| **Até (minuto)** | 38 |
| **Odd mínima** | 1.40 |
| **Filtro de Placar** | Empate 0x0 |

#### Passo 3 - Condições AO VIVO:

| Condição | Aplicado a | Operador | Valor |
|----------|------------|----------|-------|
| Ataques Perigosos | Ambos Somados | Maior que | 20 |
| Chutes no Gol | Ambos Somados | Maior que | 3 |
| Total de Chutes | Ambos Somados | Maior que | 8 |
| Posse de Bola (%) | Qualquer Time | Entre | 35% - 65% |

#### Passo 3 - Condições PRÉ-JOGO:

| Condição | Aplicado a | Operador | Valor |
|----------|------------|----------|-------|
| Média de Gols (1T) | Total | Maior que | 0.8 |
| Prognóstico Over 0.5 (1T) | - | Maior que | 55 |
| Média de Chutes ao Gol (1T) | Total | Maior que | 2.5 |

**Por que funciona**: O jogo está 0x0 mas ambos os times estão atacando bem (20+ ataques perigosos, 3+ chutes no gol). Com posse equilibrada, ambos têm chances. O histórico mostra que costumam fazer gols no 1T.

---

### 🎯 BOT 2: "Ataque Dominante 1T - Over 0.5"

**Conceito**: Identifica jogos onde um time está dominando ofensivamente mas ainda não marcou.

#### Passo 1 - Informações Básicas:
| Campo | Valor |
|-------|-------|
| **Mercado** | Mais um gol até o fim do primeiro tempo |

#### Passo 2 - Configuração Essencial:
| Campo | Valor |
|-------|-------|
| **De (minuto)** | 20 |
| **Até (minuto)** | 40 |
| **Odd mínima** | 1.50 |
| **Filtro de Placar** | Empate 0x0 |

#### Passo 3 - Condições AO VIVO:

| Condição | Aplicado a | Operador | Valor |
|----------|------------|----------|-------|
| Ataques Perigosos | Favorito | Maior que | 15 |
| Chutes no Gol | Favorito | Maior que | 3 |
| Chutes Dentro da Área | Favorito | Maior que | 2 |
| Barra de Pressão | Favorito | Maior que | 65% |
| Escanteios | Favorito | Maior que | 2 |

#### Passo 3 - Condições PRÉ-JOGO:

| Condição | Aplicado a | Operador | Valor |
|----------|------------|----------|-------|
| Prognóstico Casa Vence 1T ou Fora Vence 1T | Favorito | Maior que | 40 |
| Média de Gols (1T) | Favorito | Maior que | 0.7 |

**Por que funciona**: O favorito está pressionando fortemente (65%+ pressão), finalizando bem (3+ chutes no gol, 2+ dentro da área), e já tem escanteios. É questão de tempo até o gol sair.

---

## ⚽ CATEGORIA 2: BOTS DE GOLS NO SEGUNDO TEMPO (2 Bots)

### 🎯 BOT 3: "Virada 2T - Jogo Travado"

**Conceito**: Jogos que terminaram 0x0 no primeiro tempo mas têm histórico de gols no segundo tempo.

#### Passo 1 - Informações Básicas:
| Campo | Valor |
|-------|-------|
| **Mercado** | Mais um gol até o fim do segundo tempo |

#### Passo 2 - Configuração Essencial:
| Campo | Valor |
|-------|-------|
| **De (minuto)** | 46 |
| **Até (minuto)** | 65 |
| **Odd mínima** | 1.35 |
| **Filtro de Placar** | Empate 0x0 |

#### Passo 3 - Condições AO VIVO:

| Condição | Aplicado a | Operador | Valor |
|----------|------------|----------|-------|
| Ataques Perigosos | Ambos Somados | Maior que | 30 |
| Total de Chutes | Ambos Somados | Maior que | 12 |
| Chutes no Gol | Ambos Somados | Maior que | 4 |
| Defesas do Goleiro | Ambos Somados | Maior que | 3 |

#### Passo 3 - Condições PRÉ-JOGO:

| Condição | Aplicado a | Operador | Valor |
|----------|------------|----------|-------|
| Média de Gols | Total | Maior que | 2.0 |
| Prognóstico Over 1.5 | - | Maior que | 60 |
| Prognóstico Ambas Marcam (Sim) | - | Maior que | 45 |

**Por que funciona**: O jogo teve muitas chances no 1T (12+ chutes, 4+ no gol, goleiros trabalhando) mas ainda está 0x0. Times com média de 2+ gols tendem a abrir o placar no 2T após pressão acumulada.

---

### 🎯 BOT 4: "Explosão 2T - Over 1.5 no Jogo"

**Conceito**: Jogos que já têm 1 gol e vão ter mais pelo ritmo intenso.

#### Passo 1 - Informações Básicas:
| Campo | Valor |
|-------|-------|
| **Mercado** | Mais um gol até o fim do segundo tempo |

#### Passo 2 - Configuração Essencial:
| Campo | Valor |
|-------|-------|
| **De (minuto)** | 50 |
| **Até (minuto)** | 75 |
| **Odd mínima** | 1.45 |
| **Filtro de Placar** | Casa Vencendo OU Fora Vencendo (diferença de 1 gol) |

#### Passo 3 - Condições AO VIVO:

| Condição | Aplicado a | Operador | Valor |
|----------|------------|----------|-------|
| Ataques Perigosos | Ambos Somados | Maior que | 35 |
| Ataques perigosos 5 minutos | Ambos Somados | Maior que | 1.5 |
| Chutes no Gol | Ambos Somados | Maior que | 5 |
| Posse de Bola (%) | Zebra | Maior que | 40% |

#### Passo 3 - Condições PRÉ-JOGO:

| Condição | Aplicado a | Operador | Valor |
|----------|------------|----------|-------|
| Média de Gols | Total | Maior que | 2.3 |
| Prognóstico Over 2.5 | - | Maior que | 50 |

**Por que funciona**: Com 1 gol já marcado, o time perdedor (zebra com 40%+ posse) está atacando para empatar. A média de ataques perigosos nos últimos 5 min mostra intensidade atual. Histórico de jogos com muitos gols.

---

## 🚩 CATEGORIA 3: BOTS DE ESCANTEIOS (2 Bots)

### 🎯 BOT 5: "Pressão nas Laterais 1T - Over Escanteios"

**Conceito**: Identifica jogos com muita pressão nas laterais que geram escanteios.

#### Passo 1 - Informações Básicas:
| Campo | Valor |
|-------|-------|
| **Mercado** | Mais um escanteio até o fim do primeiro tempo |

#### Passo 2 - Configuração Essencial:
| Campo | Valor |
|-------|-------|
| **De (minuto)** | 15 |
| **Até (minuto)** | 38 |
| **Odd mínima** | 1.50 |
| **Filtro de Placar** | Qualquer |

#### Passo 3 - Condições AO VIVO:

| Condição | Aplicado a | Operador | Valor |
|----------|------------|----------|-------|
| Escanteios | Ambos Somados | Maior que | 4 |
| Ataques Perigosos | Ambos Somados | Maior que | 18 |
| Chutes Fora do Gol | Ambos Somados | Maior que | 3 |
| Chutes Bloqueados | Ambos Somados | Maior que | 2 |
| Laterais | Ambos Somados | Maior que | 15 |

#### Passo 3 - Condições PRÉ-JOGO:

| Condição | Aplicado a | Operador | Valor |
|----------|------------|----------|-------|
| Média de Escanteios (1T) | Total | Maior que | 4.0 |
| Média de Ataques Perigosos (1T) | Total | Maior que | 20 |

**Por que funciona**: Jogos com muitos chutes bloqueados e chutes para fora geram escanteios. O ritmo de laterais (15+) mostra jogo aberto nas laterais. O histórico confirma que são times que geram muitos escanteios.

---

### 🎯 BOT 6: "Domínio Lateral 2T - Over Escanteios"

**Conceito**: Identifica jogos no segundo tempo com pressão constante que gera escanteios.

#### Passo 1 - Informações Básicas:
| Campo | Valor |
|-------|-------|
| **Mercado** | Mais um escanteio até o fim do segundo tempo |

#### Passo 2 - Configuração Essencial:
| Campo | Valor |
|-------|-------|
| **De (minuto)** | 50 |
| **Até (minuto)** | 80 |
| **Odd mínima** | 1.45 |
| **Filtro de Placar** | Qualquer |

#### Passo 3 - Condições AO VIVO:

| Condição | Aplicado a | Operador | Valor |
|----------|------------|----------|-------|
| Escanteios | Ambos Somados | Maior que | 7 |
| Ataques Perigosos | Ambos Somados | Maior que | 40 |
| Total de Chutes | Ambos Somados | Maior que | 15 |
| Chutes Bloqueados | Ambos Somados | Maior que | 4 |
| Barra de Pressão | Qualquer Time | Maior que | 60% |

#### Passo 3 - Condições PRÉ-JOGO:

| Condição | Aplicado a | Operador | Valor |
|----------|------------|----------|-------|
| Média de Escanteios | Total | Maior que | 9.0 |
| Prognóstico Média de Escanteios | - | Maior que | 9 |

**Por que funciona**: Jogos que já têm 7+ escanteios, com muitos chutes bloqueados (4+) e alta pressão (60%+), tendem a continuar gerando escanteios. O histórico de 9+ escanteios por jogo confirma a tendência.

---

## 🏆 CATEGORIA 4: BOTS DE VENCEDOR (2 Bots)

### 🎯 BOT 7: "Favorito Dominante - Vitória Segura"

**Conceito**: Identifica jogos onde o favorito está dominando completamente e vai vencer.

#### Passo 1 - Informações Básicas:
| Campo | Valor |
|-------|-------|
| **Mercado** | Resultado Final - Vitória do Favorito |

#### Passo 2 - Configuração Essencial:
| Campo | Valor |
|-------|-------|
| **De (minuto)** | 25 |
| **Até (minuto)** | 60 |
| **Odd mínima** | 1.30 |
| **Filtro de Placar** | Favorito Vencendo (diferença de 1 gol) |

#### Passo 3 - Condições AO VIVO:

| Condição | Aplicado a | Operador | Valor |
|----------|------------|----------|-------|
| Posse de Bola (%) | Favorito | Maior que | 55% |
| Ataques Perigosos | Favorito | Maior que | 18 |
| Chutes no Gol | Favorito | Maior que | 4 |
| Barra de Pressão | Favorito | Maior que | 70% |
| Ataques Perigosos | Zebra | Menor que | 12 |
| Chutes no Gol | Zebra | Menor que | 3 |

#### Passo 3 - Condições PRÉ-JOGO:

| Condição | Aplicado a | Operador | Valor |
|----------|------------|----------|-------|
| Prognóstico Casa Vence ou Fora Vence | Favorito | Maior que | 60 |
| Média de Gols | Favorito | Maior que | 1.3 |

**Por que funciona**: O favorito já está vencendo, dominando posse (55%+), pressão (70%+), com muitos chutes (4+ no gol) enquanto a zebra mal consegue atacar (menos de 12 ataques perigosos e 3 chutes). Domínio total = vitória segura.

---

### 🎯 BOT 8: "Zebra Perigosa - Empate ou Virada"

**Conceito**: Identifica jogos onde a zebra está perdendo por pouco mas está jogando bem e pode empatar/virar.

#### Passo 1 - Informações Básicas:
| Campo | Valor |
|-------|-------|
| **Mercado** | Resultado Final - Dupla Chance (Zebra ou Empate) |

#### Passo 2 - Configuração Essencial:
| Campo | Valor |
|-------|-------|
| **De (minuto)** | 50 |
| **Até (minuto)** | 75 |
| **Odd mínima** | 1.60 |
| **Filtro de Placar** | Favorito Vencendo (diferença de 1 gol) |

#### Passo 3 - Condições AO VIVO:

| Condição | Aplicado a | Operador | Valor |
|----------|------------|----------|-------|
| Posse de Bola (%) | Zebra | Maior que | 45% |
| Ataques Perigosos | Zebra | Maior que | 20 |
| Chutes no Gol | Zebra | Maior que | 4 |
| Ataques perigosos 10 minutos | Zebra | Maior que | 1.2 |
| Barra de Pressão | Zebra | Maior que | 55% |
| Chutes Dentro da Área | Zebra | Maior que | 3 |

#### Passo 3 - Condições PRÉ-JOGO:

| Condição | Aplicado a | Operador | Valor |
|----------|------------|----------|-------|
| Prognóstico Fora ou Empate ou Casa ou Empate | Zebra | Maior que | 35 |
| Média de Gols | Zebra | Maior que | 1.0 |

**Por que funciona**: A zebra está perdendo por apenas 1 gol, mas está pressionando muito: 45%+ posse, 20+ ataques perigosos, 4+ chutes no gol, e pressão atual alta (1.2+ ataques/min nos últimos 10 min). Isso indica que o empate ou virada é provável.

---

## 📊 RESUMO DOS 8 BOTS

| # | Nome do Bot | Categoria | Mercado | Minutos | Placar |
|---|-------------|-----------|---------|---------|--------|
| 1 | Pressão Total 1T | Gols 1T | Over 0.5 1T | 15-38 | 0x0 |
| 2 | Ataque Dominante 1T | Gols 1T | Over 0.5 1T | 20-40 | 0x0 |
| 3 | Virada 2T | Gols 2T | Over 0.5 2T | 46-65 | 0x0 |
| 4 | Explosão 2T | Gols 2T | Over 1.5 | 50-75 | 1x0 ou 0x1 |
| 5 | Pressão nas Laterais 1T | Escanteios | Over Escanteios 1T | 15-38 | Qualquer |
| 6 | Domínio Lateral 2T | Escanteios | Over Escanteios 2T | 50-80 | Qualquer |
| 7 | Favorito Dominante | Vencedor | Vitória Favorito | 25-60 | Favorito +1 |
| 8 | Zebra Perigosa | Vencedor | Dupla Chance | 50-75 | Favorito +1 |

---

## 💡 DICAS PARA MAXIMIZAR RESULTADOS

### Gestão de Banca:
- Use no máximo 2-3% da banca por entrada
- Nunca persiga perdas
- Defina um stop loss diário (ex: -5 unidades)
- Defina um stop gain diário (ex: +3 unidades)

### Horários Recomendados:
- **Melhores ligas**: Premier League, La Liga, Serie A, Bundesliga, Ligue 1
- **Evitar**: Ligas muito fracas ou com poucos dados históricos
- **Horários nobres**: 12h-22h (horário de Brasília) para ligas europeias

### Monitoramento:
- Acompanhe o ROI de cada bot separadamente
- Após 100 entradas, avalie se precisa ajustar condições
- Desative bots com ROI negativo após 200 entradas

### Ajustes Finos:
- Se o bot não encontra jogos, relaxe 1-2 condições
- Se o bot tem muitas perdas, adicione 1-2 condições mais restritivas
- Teste um bot por vez para isolar resultados

---

## ⚠️ AVISOS IMPORTANTES

1. **Apostas envolvem risco**: Nunca aposte mais do que pode perder
2. **Resultados passados não garantem resultados futuros**
3. **Teste os bots em modo simulação antes de apostar dinheiro real**
4. **Ajuste as condições baseado nos seus resultados**
5. **Mantenha registros detalhados de todas as entradas**

---

*Documento criado para uso com SokkerPro Bot - https://go.sokkerpro.com*
