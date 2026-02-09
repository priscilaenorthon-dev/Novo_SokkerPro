# 🚀 Guia de Instalação e Configuração

## 📋 Como Configurar os Bots na Plataforma SokkerPro

### Passo 1: Acesso à Plataforma

1. Acesse https://go.sokkerpro.com
2. Faça login na sua conta
3. Navegue até a seção de **Bots**

---

## 🤖 Configuração de um Bot

### Exemplo: Bot 1 - Over 0.5 Gols 1T

Vamos configurar o Bot 1 como exemplo. O processo é similar para todos os outros.

---

### 📁 Passo 2: Criar Novo Bot

1. Clique em **"Criar Novo Bot"**
2. Dê um nome: **"Bot 1 - Over 0.5 Gols 1T (Conservador)"**

---

### 🎯 Passo 3: Configurar o Mercado (Passo 1 da Plataforma)

Segundo o arquivo `bot1_over05_goals_1T.json`:

```json
"mercado": "Mais um gol até o fim do primeiro tempo"
```

Na plataforma:
- **Mercado de Gols** → Selecione: **"Mais um gol até o fim do primeiro tempo"**

---

### ⚙️ Passo 4: Configuração Essencial (Passo 2 da Plataforma)

Segundo o JSON:
```json
"configuracao_essencial": {
  "faixa_minutos": {
    "de": 8,
    "ate": 38
  },
  "odd_minima_entrada": 1.30,
  "valor_entrada": 0,
  "filtro_placar": {
    "tipo": "Empate"
  }
}
```

Na plataforma configure:

**Faixa de Minutos:**
- **De:** 8
- **Até:** 38

**Odd Mínima de Entrada:**
- **Valor:** 1.30

**Valor de Entrada:**
- **IMPORTANTE**: Deixe em **0** (zero) inicialmente
- **Por quê?** Com valor 0, o bot apenas gera **ALERTAS** sem calcular lucro/prejuízo
- **Quando mudar?** Após validar que o bot funciona bem (depois de 20-30 alertas), configure o valor real que deseja apostar (ex: 10, 20, 50)

**Filtro de Placar:**
- Selecione: **Empate**
- Isso significa que o bot só vai alertar quando o jogo estiver **0x0**

---

### 📊 Passo 5: Condições AO VIVO (Passo 3 da Plataforma)

Estas são as condições que o jogo precisa atender EM TEMPO REAL para o bot alertar.

#### 5.1 Ataques

**Ataques Perigosos Totais:**
- Aplicado a: **Ambos Somados**
- Mínimo: **8**

**Ataques Perigosos 5 minutos:**
- Aplicado a: **Qualquer Time**
- Mínimo: **1.5**

#### 5.2 Chutes

**Chutes no Gol:**
- Aplicado a: **Ambos Somados**
- Mínimo: **3**

**Chutes Dentro da Área:**
- Aplicado a: **Ambos Somados**
- Mínimo: **2**

#### 5.3 Escanteios

**Escanteios Totais:**
- Aplicado a: **Ambos Somados**
- Mínimo: **2**

#### 5.4 Outros

**Barra de Pressão:**
- Aplicado a: **Qualquer Time**
- Mínimo: **65**

---

### 📈 Passo 6: Condições PRÉ-JOGO (Passo 3 continuação)

Estas condições são baseadas no HISTÓRICO dos times (últimos 5 jogos).

#### 6.1 Prognósticos - Gols

**Prognóstico Over 0.5 (1T):**
- Mínimo: **55**

**Prognóstico Over 1.5:**
- Mínimo: **60**

#### 6.2 Prognósticos - Resultado

**Prognóstico Casa ou Fora:**
- Mínimo: **55**

#### 6.3 Médias H2H - Gols

**Média de Gols (1T):**
- Aplicado a: **Ambos Somados**
- Mínimo: **0.8**

#### 6.4 Médias H2H - Chutes

**Média de Chutes Totais (1T):**
- Aplicado a: **Ambos Somados**
- Mínimo: **10**

**Média de Chutes ao Gol (1T):**
- Aplicado a: **Ambos Somados**
- Mínimo: **4**

---

### ✅ Passo 7: Revisar e Salvar

1. Revise TODAS as configurações
2. Confirme que todos os valores estão corretos
3. Clique em **"Salvar Bot"**
4. **Ative** o bot

---

## 🔔 Passo 8: Monitorar Alertas

### Fase 1: Teste (Primeiras 2 semanas)

- ✅ **valor_entrada: 0** (apenas alertas)
- ✅ Anote TODOS os alertas em uma planilha
- ✅ Valide manualmente se as condições estão corretas
- ✅ Acompanhe o resultado do jogo

**Exemplo de Planilha:**

| Data | Hora | Jogo | Minuto | Odd | Resultado | Green? |
|------|------|------|--------|-----|-----------|--------|
| 09/02 | 15:30 | Time A x Time B | 15' | 1.35 | 1x0 | ✅ SIM |
| 09/02 | 18:00 | Time C x Time D | 22' | 1.28 | 0x0 | ❌ NÃO |

### Fase 2: Validação (Semanas 3-4)

- ✅ Se taxa de acerto >= 65%, continue
- ✅ Se < 65%, revise as condições
- ✅ Configure **valor_entrada** com 1-2% da sua banca
- ✅ Exemplo: Banca de 1000 → valor_entrada: 10 ou 20

### Fase 3: Operação (Mês 2+)

- ✅ Aumente gradualmente o valor_entrada
- ✅ Nunca mais que 3% por entrada
- ✅ Diversifique entre múltiplos bots

---

## 📋 Checklist de Configuração

Antes de ativar o bot, confirme:

- [ ] Nome do bot está configurado
- [ ] Mercado correto selecionado
- [ ] Faixa de minutos: De 8 até 38
- [ ] Odd mínima: 1.30
- [ ] Valor de entrada: 0 (para teste)
- [ ] Filtro de placar: Empate
- [ ] TODAS as condições AO VIVO configuradas (6 condições)
- [ ] TODAS as condições PRÉ-JOGO configuradas (6 condições)
- [ ] Bot salvo
- [ ] Bot ativado

---

## 🎯 Configuração Rápida dos Outros Bots

### Bot 2: Asian Over 0.5 Gols 1T

**Principais Diferenças:**
- Mercado: **"Mais um gol asiático até o fim do primeiro tempo"**
- Faixa: 5 a 40
- Odd mínima: 1.25
- Condições mais flexíveis (6+ ataques perigosos)

### Bot 3: Over 0.5 Escanteios 1T

**Principais Diferenças:**
- Mercado: **"Mais um escanteio até o fim do primeiro tempo"**
- Faixa: 10 a 42
- Odd mínima: 1.20
- Filtro de placar: **Qualquer**
- Condições focadas em escanteios

### Bot 4: Asian Over 0.5 Escanteios 1T

**Principais Diferenças:**
- Mercado: **"Mais um escanteio asiático até o fim do primeiro tempo"**
- Faixa: 8 a 43
- Odd mínima: 1.15
- Mais flexível (8+ ataques perigosos)

### Bot 5: Under 0.5 Gols 1T

**Principais Diferenças:**
- Mercado: **"Sem mais gols até o fim do primeiro tempo"**
- Faixa: 15 a 38
- Odd mínima: 1.35
- Condições são **MÁXIMOS** (não mínimos!)
- Exemplo: MÁXIMO 6 ataques perigosos

### Bot 6: Asian Under 0.5 Gols 1T

**Principais Diferenças:**
- Mercado: **"Sem mais gols (asiático) até o fim do primeiro tempo"**
- Faixa: 12 a 40
- Odd mínima: 1.30
- Condições são **MÁXIMOS** com proteção asiática

---

## 💡 Dicas Importantes

### ⚠️ Sobre "valor_entrada: 0"

**Por que começar com 0?**
- ✅ Você testa o bot SEM RISCO
- ✅ Valida se as condições estão boas
- ✅ Aprende como o bot funciona
- ✅ Ganha confiança antes de apostar dinheiro real

**Quando mudar para um valor real?**
- ✅ Após 20-30 alertas
- ✅ Se taxa de acerto >= 65-70%
- ✅ Quando entender bem o bot
- ✅ Comece com 1-2% da banca

### 📊 Sobre as Condições

**"Aplicado a" - O que significa?**
- **Ambos Somados**: Soma do time da casa + visitante
- **Qualquer Time**: Basta UM time atingir
- **Casa**: Apenas o time da casa
- **Visitante**: Apenas o time visitante

**Exemplo:**
- Ataques perigosos totais: 8+ (Ambos Somados)
- Significa: Time A tem 5 + Time B tem 3 = 8 ✅ OK
- OU: Time A tem 8 + Time B tem 0 = 8 ✅ OK

### 🔄 Sobre Bots Asiáticos

**O que muda?**
- Se o resultado for EXATAMENTE o número do asiático → **DEVOLVE** o stake
- Exemplo Bot 2: Se sair 1 gol no 1T → você recupera o que apostou (push)
- Para ganhar: precisa sair 2+ gols
- Para perder: jogo fica 0x0

**Vantagem:** MUITO mais seguro, menos perdas totais

---

## 📱 Resumo: 3 Passos para Começar

### 1️⃣ Configure 2 Bots (15-20 minutos)
- Escolha: Bot 3 (Escanteios) e Bot 2 (Asian Gols)
- Use **valor_entrada: 0**

### 2️⃣ Monitore por 2 Semanas
- Anote todos os alertas
- Valide se as taxas de acerto são boas (>65%)

### 3️⃣ Comece a Operar
- Configure valor_entrada (1-2% da banca)
- Adicione mais bots gradualmente
- Escale conforme resultados

---

## ✅ Pronto para Começar!

1. ✅ Leia este guia completo
2. ✅ Escolha 2-3 bots para começar
3. ✅ Configure na plataforma SokkerPro
4. ✅ Teste com valor_entrada: 0
5. ✅ Monitore e aprenda
6. ✅ Escale gradualmente

**Boa sorte e bons greens! 🟢💰**

---

## 🆘 Problemas Comuns

### "Bot não está gerando alertas"
- ✅ Verifique se o bot está ATIVADO
- ✅ Verifique se TODAS as condições foram configuradas
- ✅ As condições são rigorosas - é normal ter poucos alertas (2-3 por dia)

### "Muitos alertas mas poucos greens"
- ✅ Revise se configurou corretamente as condições
- ✅ Confirme que os valores mínimos estão corretos
- ✅ Valide se aplicou as condições aos times certos (casa/visitante/ambos)

### "Odd está sempre abaixo da mínima"
- ✅ Talvez precise reduzir a odd mínima em 0.05-0.10
- ✅ Ou aguardar jogos com odds melhores

---

**Documentação completa em**: 
- GUIA_BOTS.md
- GUIA_RAPIDO.md
- TABELA_RESUMO.md
