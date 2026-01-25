# 🤖 12 BOTS CONFIGURADOS SOKKERPRO

> **Requisito:** Odds mínimas de **1.50** para todas as entradas
> **Objetivo:** Maximizar chances de GREEN com condições bem analisadas

---

## 📋 ÍNDICE

1. [Bots de Gols no Primeiro Tempo](#-bots-de-gols-no-primeiro-tempo)
2. [Bots de Gols no Segundo Tempo](#-bots-de-gols-no-segundo-tempo)
3. [Bots de Escanteios](#-bots-de-escanteios)
4. [Bots de Vencedor](#-bots-de-vencedor)

---

## ⚽ BOTS DE GOLS NO PRIMEIRO TEMPO

### 🟢 BOT 1: Over 0.5 1T - Conservador

**Mercado:** Mais um gol até o fim do primeiro tempo

**Objetivo:** Entrar em jogos com alta probabilidade de gol no 1º tempo

#### Configuração Essencial:
| Campo | Valor |
|-------|-------|
| De (Minuto) | 5 |
| Até (Minuto) | 25 |
| Odd Mínima | 1.50 |
| Filtro de Placar | Empate (0x0) |

#### Condições AO VIVO (Ambos Somados):
| Condição | Operador | Valor |
|----------|----------|-------|
| Ataques Perigosos | ≥ | 15 |
| Chutes no Gol | ≥ | 3 |
| Chutes Totais | ≥ | 6 |
| Barra de Pressão | ≥ | 60% |

#### Condições PRÉ-JOGO:
| Condição | Operador | Valor |
|----------|----------|-------|
| Prognóstico Over 0.5 (1T) | ≥ | 65 |
| Média de Gols (1T) | ≥ | 0.8 |

#### Passo a Passo para Adicionar:
1. Acesse https://go.sokkerpro.com
2. Clique em "Criar Bot"
3. **Informações Básicas:** Selecione "Mais um gol até o fim do primeiro tempo"
4. **Faixa de Minutos:** De: 5 | Até: 25
5. **Odd Mínima:** 1.50
6. **Filtro de Placar:** Empate
7. **Condições AO VIVO:** Adicione cada condição conforme tabela acima (selecione "Ambos Somados")
8. **Condições PRÉ-JOGO:** Adicione prognósticos e médias conforme tabela
9. Salve o bot

---

### 🟢 BOT 2: Over 0.5 1T - Agressivo

**Mercado:** Mais um gol até o fim do primeiro tempo

**Objetivo:** Entrar mais cedo em jogos com pressão alta

#### Configuração Essencial:
| Campo | Valor |
|-------|-------|
| De (Minuto) | 10 |
| Até (Minuto) | 35 |
| Odd Mínima | 1.50 |
| Filtro de Placar | Empate (0x0) |

#### Condições AO VIVO (Ambos Somados):
| Condição | Operador | Valor |
|----------|----------|-------|
| Ataques Perigosos | ≥ | 20 |
| Ataques Perigosos 5 min | ≥ | 2.5 |
| Chutes no Gol | ≥ | 4 |
| Chutes Dentro da Área | ≥ | 3 |
| Barra de Pressão | ≥ | 65% |

#### Condições PRÉ-JOGO:
| Condição | Operador | Valor |
|----------|----------|-------|
| Prognóstico Over 0.5 (1T) | ≥ | 70 |
| Média de Gols (1T) | ≥ | 1.0 |
| Média de Ataques Perigosos (1T) | ≥ | 40 |

#### Passo a Passo:
1. Mesmo processo do Bot 1
2. Ajuste os valores conforme tabelas acima
3. Este bot é mais seletivo e entra em menos jogos, mas com maior confiança

---

### 🟢 BOT 3: Over 1.5 1T - Alta Probabilidade

**Mercado:** Mais de 1.5 gols no primeiro tempo

**Objetivo:** Buscar jogos com 2+ gols no primeiro tempo (odds geralmente melhores)

#### Configuração Essencial:
| Campo | Valor |
|-------|-------|
| De (Minuto) | 15 |
| Até (Minuto) | 40 |
| Odd Mínima | 1.50 |
| Filtro de Placar | Qualquer (com pelo menos 1 gol) |

#### Condições AO VIVO (Ambos Somados):
| Condição | Operador | Valor |
|----------|----------|-------|
| Ataques Perigosos | ≥ | 25 |
| Chutes no Gol | ≥ | 5 |
| Chutes Totais | ≥ | 10 |
| Ataques Perigosos 3 min | ≥ | 2.0 |
| Escanteios | ≥ | 4 |
| Barra de Pressão | ≥ | 65% |

#### Condições PRÉ-JOGO:
| Condição | Operador | Valor |
|----------|----------|-------|
| Prognóstico Over 1.5 (1T) | ≥ | 55 |
| Média de Gols (1T) | ≥ | 1.2 |
| Média de Chutes ao Gol (1T) | ≥ | 3.0 |

#### Passo a Passo:
1. Mesmo processo do Bot 1
2. Importante: Este bot funciona melhor quando já há 1 gol no jogo
3. Use filtro de placar "Casa Vencendo" OU "Fora Vencendo" OU "Empate" (1x1, 2x2)

---

## ⚽ BOTS DE GOLS NO SEGUNDO TEMPO

### 🟡 BOT 4: Over 0.5 2T - Conservador

**Mercado:** Mais um gol até o fim do jogo (entrada no 2º tempo)

**Objetivo:** Entrar no início do 2º tempo em jogos aquecidos

#### Configuração Essencial:
| Campo | Valor |
|-------|-------|
| De (Minuto) | 46 |
| Até (Minuto) | 60 |
| Odd Mínima | 1.50 |
| Filtro de Placar | Qualquer |

#### Condições AO VIVO (Ambos Somados):
| Condição | Operador | Valor |
|----------|----------|-------|
| Ataques Perigosos | ≥ | 30 |
| Chutes no Gol | ≥ | 4 |
| Chutes Totais | ≥ | 10 |
| Ataques Perigosos 5 min | ≥ | 2.0 |
| Barra de Pressão | ≥ | 55% |

#### Condições PRÉ-JOGO:
| Condição | Operador | Valor |
|----------|----------|-------|
| Prognóstico Over 1.5 | ≥ | 60 |
| Média de Gols | ≥ | 2.0 |

#### Passo a Passo:
1. Acesse https://go.sokkerpro.com
2. Crie novo bot com mercado "Mais um gol até o fim do jogo"
3. Configure faixa de minutos: 46 a 60
4. Adicione todas as condições das tabelas
5. Este bot analisa o 1º tempo e entra logo no início do 2º

---

### 🟡 BOT 5: Over 0.5 2T - Agressivo

**Mercado:** Mais um gol até o fim do jogo

**Objetivo:** Buscar gols quando um time está pressionando forte

#### Configuração Essencial:
| Campo | Valor |
|-------|-------|
| De (Minuto) | 50 |
| Até (Minuto) | 75 |
| Odd Mínima | 1.50 |
| Filtro de Placar | Empate OU Favorito Perdendo (diferença: 1) |

#### Condições AO VIVO (Qualquer Time):
| Condição | Operador | Valor |
|----------|----------|-------|
| Ataques Perigosos | ≥ | 20 |
| Chutes no Gol | ≥ | 5 |
| Ataques Perigosos 5 min | ≥ | 3.0 |
| Barra de Pressão | ≥ | 70% |

#### Condições AO VIVO (Ambos Somados):
| Condição | Operador | Valor |
|----------|----------|-------|
| Chutes Totais | ≥ | 15 |
| Escanteios | ≥ | 6 |

#### Condições PRÉ-JOGO:
| Condição | Operador | Valor |
|----------|----------|-------|
| Prognóstico Over 2.5 | ≥ | 50 |
| Média de Gols | ≥ | 2.5 |

---

### 🟡 BOT 6: Mais 1 Gol 2T - Alta Pressão

**Mercado:** Mais um gol asiático até o fim do jogo

**Objetivo:** Entrada em jogos com pressão extrema - recupera valor se sair apenas 1 gol

#### Configuração Essencial:
| Campo | Valor |
|-------|-------|
| De (Minuto) | 55 |
| Até (Minuto) | 80 |
| Odd Mínima | 1.50 |
| Filtro de Placar | Favorito Perdendo OU Empate |

#### Condições AO VIVO (Favorito/Zebra - Favorito):
| Condição | Operador | Valor |
|----------|----------|-------|
| Ataques Perigosos | ≥ | 35 |
| Chutes no Gol | ≥ | 7 |
| Ataques Perigosos 10 min | ≥ | 3.5 |
| Barra de Pressão | ≥ | 75% |
| Posse de Bola | ≥ | 55% |

#### Condições PRÉ-JOGO:
| Condição | Operador | Valor |
|----------|----------|-------|
| Prognóstico Casa/Fora Vence | ≥ | 65 |
| Média de Gols | ≥ | 2.0 |

#### Passo a Passo:
1. Este bot usa mercado ASIÁTICO - devolve se sair só 1 gol
2. Ideal para jogos onde o favorito está perdendo e pressionando
3. Menor risco de loss completo

---

## 🔵 BOTS DE ESCANTEIOS

### 🔷 BOT 7: Mais 1 Escanteio 1T - Conservador

**Mercado:** Mais um escanteio até o fim do primeiro tempo

**Objetivo:** Entrar quando há pressão lateral constante

#### Configuração Essencial:
| Campo | Valor |
|-------|-------|
| De (Minuto) | 10 |
| Até (Minuto) | 35 |
| Odd Mínima | 1.50 |
| Filtro de Placar | Qualquer |

#### Condições AO VIVO (Ambos Somados):
| Condição | Operador | Valor |
|----------|----------|-------|
| Escanteios | ≥ | 3 |
| Ataques Perigosos | ≥ | 18 |
| Chutes Fora do Gol | ≥ | 3 |
| Chutes Bloqueados | ≥ | 2 |

#### Condições PRÉ-JOGO:
| Condição | Operador | Valor |
|----------|----------|-------|
| Média de Escanteios (1T) | ≥ | 4.0 |
| Média de Ataques Perigosos (1T) | ≥ | 35 |

#### Passo a Passo:
1. Escanteios vêm de chutes bloqueados e fora do gol
2. Configure as condições que indicam pressão sem finalização certeira
3. Um escanteio aumenta ~2% chance de gol e ~15% nos próximos 5 min

---

### 🔷 BOT 8: Mais 1 Escanteio 1T - Agressivo

**Mercado:** Mais um escanteio até o fim do primeiro tempo

**Objetivo:** Buscar jogos com ritmo intenso de escanteios

#### Configuração Essencial:
| Campo | Valor |
|-------|-------|
| De (Minuto) | 15 |
| Até (Minuto) | 38 |
| Odd Mínima | 1.50 |
| Filtro de Placar | Qualquer |

#### Condições AO VIVO (Qualquer Time):
| Condição | Operador | Valor |
|----------|----------|-------|
| Escanteios | ≥ | 3 |
| Ataques Perigosos | ≥ | 15 |
| Chutes Totais | ≥ | 5 |
| Barra de Pressão | ≥ | 60% |

#### Condições AO VIVO (Ambos Somados):
| Condição | Operador | Valor |
|----------|----------|-------|
| Escanteios | ≥ | 5 |
| Ataques Perigosos | ≥ | 25 |

#### Condições PRÉ-JOGO:
| Condição | Operador | Valor |
|----------|----------|-------|
| Média de Escanteios (1T) | ≥ | 5.0 |
| Prognóstico Média Escanteios | ≥ | 9 |

---

### 🔷 BOT 9: Mais 1 Escanteio 2T

**Mercado:** Mais um escanteio até o fim do jogo (2º tempo)

**Objetivo:** Aproveitar ritmo de jogo estabelecido no 1º tempo

#### Configuração Essencial:
| Campo | Valor |
|-------|-------|
| De (Minuto) | 46 |
| Até (Minuto) | 70 |
| Odd Mínima | 1.50 |
| Filtro de Placar | Qualquer |

#### Condições AO VIVO (Ambos Somados):
| Condição | Operador | Valor |
|----------|----------|-------|
| Escanteios | ≥ | 6 |
| Ataques Perigosos | ≥ | 40 |
| Chutes Totais | ≥ | 12 |
| Chutes Fora do Gol | ≥ | 4 |
| Chutes Bloqueados | ≥ | 3 |

#### Condições PRÉ-JOGO:
| Condição | Operador | Valor |
|----------|----------|-------|
| Média de Escanteios | ≥ | 9.0 |
| Prognóstico Média Escanteios | ≥ | 9 |

#### Passo a Passo:
1. Este bot analisa todo o 1º tempo de escanteios
2. Se teve 6+ escanteios no 1T, tendência é continuar
3. Jogos com muitos chutes fora/bloqueados = mais escanteios

---

## 🏆 BOTS DE VENCEDOR

### 🥇 BOT 10: Casa Vence (Favorito)

**Mercado:** 1X2 - Casa Vence

**Objetivo:** Apoiar o favorito em casa quando está pressionando

#### Configuração Essencial:
| Campo | Valor |
|-------|-------|
| De (Minuto) | 60 |
| Até (Minuto) | 80 |
| Odd Mínima | 1.50 |
| Filtro de Placar | Empate OU Favorito Perdendo (diferença: 1) |

#### Condições AO VIVO (Casa):
| Condição | Operador | Valor |
|----------|----------|-------|
| Ataques Perigosos | ≥ | 40 |
| Chutes no Gol | ≥ | 8 |
| Ataques Perigosos 10 min | ≥ | 3.0 |
| Barra de Pressão | ≥ | 70% |
| Posse de Bola | ≥ | 55% |
| Chutes Dentro da Área | ≥ | 6 |

#### Condições PRÉ-JOGO:
| Condição | Operador | Valor |
|----------|----------|-------|
| Prognóstico Casa Vence | ≥ | 60 |
| Média de Gols (Casa) | ≥ | 1.5 |

#### Passo a Passo:
1. Este bot é para quando você quer apostar no resultado final
2. Entra só quando a casa é favorita e está dominando
3. Ideal para odds de 1.50 a 2.50 com alta confiança

---

### 🥇 BOT 11: Fora Vence (Favorito Visitante)

**Mercado:** 1X2 - Fora Vence

**Objetivo:** Apoiar visitante favorito quando domina o jogo

#### Configuração Essencial:
| Campo | Valor |
|-------|-------|
| De (Minuto) | 60 |
| Até (Minuto) | 80 |
| Odd Mínima | 1.50 |
| Filtro de Placar | Empate OU Favorito Perdendo (diferença: 1) |

#### Condições AO VIVO (Visitante):
| Condição | Operador | Valor |
|----------|----------|-------|
| Ataques Perigosos | ≥ | 35 |
| Chutes no Gol | ≥ | 7 |
| Ataques Perigosos 10 min | ≥ | 3.0 |
| Barra de Pressão | ≥ | 65% |
| Posse de Bola | ≥ | 50% |

#### Condições PRÉ-JOGO:
| Condição | Operador | Valor |
|----------|----------|-------|
| Prognóstico Fora Vence | ≥ | 55 |
| Média de Gols (Visitante) | ≥ | 1.3 |

---

### 🥇 BOT 12: Casa ou Empate (Dupla Chance - Seguro)

**Mercado:** Dupla Chance - 1X (Casa ou Empate)

**Objetivo:** Entrada segura quando a casa está equilibrada/superior

#### Configuração Essencial:
| Campo | Valor |
|-------|-------|
| De (Minuto) | 55 |
| Até (Minuto) | 75 |
| Odd Mínima | 1.50 |
| Filtro de Placar | Casa Vencendo OU Empate |

#### Condições AO VIVO (Casa):
| Condição | Operador | Valor |
|----------|----------|-------|
| Ataques Perigosos | ≥ | 30 |
| Chutes no Gol | ≥ | 5 |
| Barra de Pressão | ≥ | 50% |
| Posse de Bola | ≥ | 45% |

#### Condições AO VIVO (Visitante - LIMITANTES):
| Condição | Operador | Valor |
|----------|----------|-------|
| Chutes no Gol | ≤ | 4 |
| Ataques Perigosos | ≤ | 25 |

#### Condições PRÉ-JOGO:
| Condição | Operador | Valor |
|----------|----------|-------|
| Prognóstico Casa ou Empate | ≥ | 65 |

#### Passo a Passo:
1. Este é um bot SEGURO - você ganha se casa vencer OU empatar
2. Odds geralmente menores, mas win rate maior
3. Adicione condições que limitam o visitante para maior segurança

---

## 📊 RESUMO DOS 12 BOTS

| # | Nome | Mercado | Minutos | Risco |
|---|------|---------|---------|-------|
| 1 | Gol 1T Conservador | Over 0.5 1T | 5-25 | ⭐⭐ |
| 2 | Gol 1T Agressivo | Over 0.5 1T | 10-35 | ⭐⭐⭐ |
| 3 | Gol 1T Over 1.5 | Over 1.5 1T | 15-40 | ⭐⭐⭐⭐ |
| 4 | Gol 2T Conservador | Over 0.5 2T | 46-60 | ⭐⭐ |
| 5 | Gol 2T Agressivo | Over 0.5 2T | 50-75 | ⭐⭐⭐ |
| 6 | Gol 2T Alta Pressão | Asiático 2T | 55-80 | ⭐⭐⭐ |
| 7 | Escanteio 1T Conservador | +1 Escanteio 1T | 10-35 | ⭐⭐ |
| 8 | Escanteio 1T Agressivo | +1 Escanteio 1T | 15-38 | ⭐⭐⭐ |
| 9 | Escanteio 2T | +1 Escanteio 2T | 46-70 | ⭐⭐ |
| 10 | Casa Vence | 1X2 Casa | 60-80 | ⭐⭐⭐⭐ |
| 11 | Fora Vence | 1X2 Fora | 60-80 | ⭐⭐⭐⭐ |
| 12 | Dupla Chance 1X | 1X | 55-75 | ⭐ |

**Legenda de Risco:**
- ⭐ = Baixo risco (maior win rate, menores odds)
- ⭐⭐ = Risco moderado
- ⭐⭐⭐ = Risco médio
- ⭐⭐⭐⭐ = Risco alto (menores win rate, maiores odds)

---

## 💡 DICAS IMPORTANTES

### Para Maximizar GREEN:

1. **Nunca entre em odds abaixo de 1.50** - Configurado em todos os bots
2. **Combine condições AO VIVO com PRÉ-JOGO** - Valida histórico + momento atual
3. **Use a Barra de Pressão** - Indicador exclusivo SokkerPRO muito confiável
4. **Escanteios após chutes bloqueados** - Alta correlação
5. **Favorito perdendo = pressão** - Ótima oportunidade
6. **Segundo tempo começa aquecido** - Use dados do 1º tempo

### Gestão de Banca:

- Defina valor de entrada fixo (ex: R$ 10 por alerta)
- Não entre em todos os alertas - analise rapidamente as odds atuais
- Bots conservadores: stake normal
- Bots agressivos: stake reduzido (50%)

### Filtros de Liga Recomendados:

Considere remover ligas com:
- Baixo volume de estatísticas
- Times muito desiguais
- Ligas amadoras ou de divisões muito baixas

---

## 🔧 PASSO A PASSO GERAL PARA ADICIONAR UM BOT

1. **Acesse** https://go.sokkerpro.com
2. **Clique** em "Criar Bot" ou "Novo Bot"
3. **Escolha o Mercado** (Gols, Escanteios, Vencedor)
4. **Configure a Faixa de Minutos** (De/Até)
5. **Defina a Odd Mínima** (≥ 1.50)
6. **Selecione o Filtro de Placar** apropriado
7. **Adicione Condições AO VIVO:**
   - Escolha "Aplicar a" (Casa/Visitante/Ambos/Qualquer/Favorito)
   - Selecione a estatística
   - Defina operador (≥, ≤, =)
   - Insira o valor
8. **Adicione Condições PRÉ-JOGO:**
   - Prognósticos e Médias H2H
9. **Salve e Ative** o bot
10. **Monitore** os alertas e ajuste conforme necessário

---

*Documento criado com base no manual oficial SokkerPRO Bots*
*Última atualização: Janeiro 2026*
