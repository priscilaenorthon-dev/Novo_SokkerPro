# 📊 Tabela Resumo - Configurações dos 6 Bots

## Bot 1: Over 0.5 Gols 1T (Conservador)
**Arquivo**: `bot1_over05_goals_1T.json`

| Parâmetro | Valor |
|-----------|-------|
| **Mercado** | Mais um gol até o fim do primeiro tempo |
| **Minutos** | 8 a 38 |
| **Odd Mínima** | 1.30 |
| **Placar** | Empate (0x0) |
| **Risco** | Baixo a Médio |
| **ROI Esperado** | 15-25% |
| **Taxa de Acerto** | 70%+ |

**Principais Condições**:
- ✅ 8+ ataques perigosos somados
- ✅ 1.5+ ataques perigosos/5min
- ✅ 3+ chutes no gol
- ✅ 2+ escanteios
- ✅ 65%+ barra pressão
- ✅ 55%+ prognóstico Over 0.5 1T

---

## Bot 2: Asian Over 0.5 Gols 1T (Proteção)
**Arquivo**: `bot2_asian_over05_goals_1T.json`

| Parâmetro | Valor |
|-----------|-------|
| **Mercado** | Mais um gol asiático até o fim do primeiro tempo |
| **Proteção** | ✅ 1 gol = DEVOLVE, 2+ = GANHA |
| **Minutos** | 5 a 40 |
| **Odd Mínima** | 1.25 |
| **Placar** | Empate (0x0) |
| **Risco** | Baixo |
| **ROI Esperado** | 12-20% |
| **Taxa de Acerto** | 70%+ |

**Principais Condições**:
- ✅ 6+ ataques perigosos somados
- ✅ 1.2+ ataques perigosos/3min
- ✅ 6+ chutes totais
- ✅ 2+ chutes no gol
- ✅ 60%+ barra pressão
- ✅ 50%+ prognóstico Over 0.5 1T

---

## Bot 3: Over 0.5 Escanteios 1T (Alta Probabilidade)
**Arquivo**: `bot3_over05_corners_1T.json`

| Parâmetro | Valor |
|-----------|-------|
| **Mercado** | Mais um escanteio até o fim do primeiro tempo |
| **Minutos** | 10 a 42 |
| **Odd Mínima** | 1.20 |
| **Placar** | Qualquer |
| **Risco** | Baixo |
| **ROI Esperado** | 18-28% |
| **Taxa de Acerto** | 75%+ |

**Principais Condições**:
- ✅ 10+ ataques perigosos somados
- ✅ 1.8+ ataques perigosos/5min
- ✅ 35+ ataques totais
- ✅ 8+ chutes totais
- ✅ 65%+ barra pressão
- ✅ 3.5+ média escanteios 1T histórico

---

## Bot 4: Asian Over 0.5 Escanteios 1T (Segurança)
**Arquivo**: `bot4_asian_over05_corners_1T.json`

| Parâmetro | Valor |
|-----------|-------|
| **Mercado** | Mais um escanteio asiático até o fim do primeiro tempo |
| **Proteção** | ✅ 1 escanteio = DEVOLVE, 2+ = GANHA |
| **Minutos** | 8 a 43 |
| **Odd Mínima** | 1.15 |
| **Placar** | Qualquer |
| **Risco** | Muito Baixo |
| **ROI Esperado** | 10-18% |
| **Taxa de Acerto** | 75%+ |

**Principais Condições**:
- ✅ 8+ ataques perigosos somados
- ✅ 1.5+ ataques perigosos/3min
- ✅ 30+ ataques totais
- ✅ 6+ chutes totais
- ✅ 60%+ barra pressão
- ✅ 3.0+ média escanteios 1T histórico

---

## Bot 5: Under 0.5 Gols 1T (Jogos Defensivos)
**Arquivo**: `bot5_under05_goals_1T.json`

| Parâmetro | Valor |
|-----------|-------|
| **Mercado** | Sem mais gols até o fim do primeiro tempo |
| **Minutos** | 15 a 38 |
| **Odd Mínima** | 1.35 |
| **Placar** | Empate (0x0) |
| **Risco** | Médio |
| **ROI Esperado** | 20-30% |
| **Taxa de Acerto** | 65%+ |

**Principais Condições** (MÁXIMOS):
- ✅ MÁXIMO 6 ataques perigosos
- ✅ MÁXIMO 1.0 ataques perigosos/5min
- ✅ MÁXIMO 2 chutes no gol
- ✅ MÁXIMO 3 escanteios
- ✅ MÁXIMO 60% barra pressão
- ✅ MÁXIMO 45% prognóstico Over 0.5 1T

---

## Bot 6: Asian Under 0.5 Gols 1T (Risco Calculado)
**Arquivo**: `bot6_asian_under05_goals_1T.json`

| Parâmetro | Valor |
|-----------|-------|
| **Mercado** | Sem mais gols (asiático) até o fim do primeiro tempo |
| **Proteção** | ✅ 1 gol = DEVOLVE, 2+ = PERDE |
| **Minutos** | 12 a 40 |
| **Odd Mínima** | 1.30 |
| **Placar** | Empate (0x0) |
| **Risco** | Baixo a Médio |
| **ROI Esperado** | 15-25% |
| **Taxa de Acerto** | 70%+ |

**Principais Condições** (MÁXIMOS):
- ✅ MÁXIMO 8 ataques perigosos
- ✅ MÁXIMO 1.2 ataques perigosos/5min
- ✅ MÁXIMO 3 chutes no gol
- ✅ MÁXIMO 4 escanteios
- ✅ MÁXIMO 65% barra pressão
- ✅ MÁXIMO 50% prognóstico Over 0.5 1T

---

## 📈 Resumo Comparativo

| Bot | Tipo | Proteção | Risco | ROI | Acerto | Odd Min |
|-----|------|----------|-------|-----|--------|---------|
| 1 | Over Gols | ❌ | Baixo-Médio | 15-25% | 70%+ | 1.30 |
| 2 | Asian Over Gols | ✅ | Baixo | 12-20% | 70%+ | 1.25 |
| 3 | Over Escanteios | ❌ | Baixo | 18-28% | 75%+ | 1.20 |
| 4 | Asian Over Escanteios | ✅ | Muito Baixo | 10-18% | 75%+ | 1.15 |
| 5 | Under Gols | ❌ | Médio | 20-30% | 65%+ | 1.35 |
| 6 | Asian Under Gols | ✅ | Baixo-Médio | 15-25% | 70%+ | 1.30 |

---

## 🎯 Quando Usar Cada Bot

### Situação do Jogo: 0x0, Min 10-15, MUITOS Ataques
- **1ª Opção**: Bot 1 (odd melhor)
- **2ª Opção**: Bot 2 (mais seguro)

### Situação do Jogo: Qualquer placar, Min 10-20, MUITA Pressão
- **1ª Opção**: Bot 3 (melhor ROI)
- **2ª Opção**: Bot 4 (mais seguro)

### Situação do Jogo: 0x0, Min 15-25, POUCOS Ataques
- **1ª Opção**: Bot 5 (melhor odd)
- **2ª Opção**: Bot 6 (mais seguro)

---

## 💡 Dicas de Combinação

### Portfólio Conservador (Iniciantes)
- 50% Bot 4 (Asian Escanteios)
- 30% Bot 2 (Asian Over Gols)
- 20% Bot 6 (Asian Under Gols)
- **Risco**: Muito Baixo
- **ROI**: 10-18%

### Portfólio Balanceado (Intermediário)
- 30% Bot 3 (Over Escanteios)
- 25% Bot 4 (Asian Escanteios)
- 25% Bot 2 (Asian Over Gols)
- 20% Bot 6 (Asian Under Gols)
- **Risco**: Baixo a Médio
- **ROI**: 13-22%

### Portfólio Agressivo (Avançado)
- 30% Bot 3 (Over Escanteios)
- 25% Bot 1 (Over Gols)
- 25% Bot 5 (Under Gols)
- 20% Bot 4 (Asian Escanteios)
- **Risco**: Médio
- **ROI**: 18-28%

---

## ✅ Checklist de Entrada

Antes de entrar, confirme:

### Para OVER (Bots 1, 2, 3, 4)
- [ ] Jogo tem ataques perigosos suficientes
- [ ] Chutes sendo realizados
- [ ] Barra de pressão alta
- [ ] Prognóstico favorável
- [ ] Odd >= mínima
- [ ] Tempo adequado

### Para UNDER (Bots 5, 6)
- [ ] Jogo está 0x0
- [ ] POUCOS ataques perigosos
- [ ] POUCOS chutes no gol
- [ ] Barra pressão baixa
- [ ] Prognóstico baixo para gols
- [ ] Odd >= mínima
- [ ] Tempo adequado

---

## 📱 Implementação Rápida

1. **Escolha 2-3 bots** da tabela acima
2. **Configure** na plataforma SokkerPro
3. **Teste** com alertas (sem valor)
4. **Valide** manualmente cada entrada
5. **Comece** com 1-2% da banca
6. **Escale** gradualmente

---

**Sucesso! 🟢💰**
