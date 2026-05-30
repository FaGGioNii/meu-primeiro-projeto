# Task: Reflexão Semanal

**Task ID:** reflexao-semanal
**Version:** 1.0
**Purpose:** Reflexão semanal baseada em hábitos, consistência e ajustes sistêmicos para a próxima semana
**Agent:** assistente-pessoal (Clara)
**Mode:** Interactive

---

## Inputs

| Parâmetro | Tipo | Obrigatório | Descrição |
|-----------|------|-------------|-----------|
| `semana_referencia` | string | Não | Semana sendo revisada (padrão: semana atual) |
| `habitos_rastreados` | map | Não | Dados de rastreamento dos hábitos da semana |
| `eventos_notaveis` | list | Não | Eventos que impactaram a semana |

---

## Steps

### Step 1: Revisar Consistência dos Hábitos

**Ação:**
- Para cada hábito rastreado, calcular taxa de consistência da semana:
  - Alta (>80%): hábito sólido — manter
  - Média (50-80%): hábito em desenvolvimento — identificar gargalo
  - Baixa (<50%): hábito frágil — diagnosticar e ajustar
- Verificar correntes quebradas: "Você falhou duas vezes seguidas em algum hábito?"
- Identificar o hábito com maior e menor consistência

**Output:** `consistencia_semanal` — taxa de cada hábito + classificação

---

### Step 2: Extrair Uma Lição Aprendida

**Ação:**
- Perguntar: "O que você aprendeu sobre seus sistemas esta semana?"
- Guiar reflexão:
  - "O que funcionou melhor do que o esperado?"
  - "O que tornou algum hábito difícil de executar?"
  - "Houve alguma situação que revelou um gargalo no seu sistema?"
- Formular a lição de forma sistêmica (sobre ambiente/sinal/hábito, não sobre força de vontade)

**Output:** `licao_aprendida` — uma lição sistêmica concreta

**Veto condition:**
- Se lição é "preciso ter mais disciplina" → reformular em termos de sistema

---

### Step 3: Identificar Um Ajuste Sistêmico

**Ação:**
- Com base na lição aprendida e na consistência, definir UM ajuste sistêmico para a próxima semana:
  - Modificação de ambiente
  - Novo sinal (cue)
  - Redução de fricção
  - Nova recompensa imediata
- Regra: apenas UM ajuste por vez — mudanças simultâneas geram confusão de causalidade
- Formular como ação concreta: "Na próxima semana, farei [ação específica] para [efeito esperado]"

**Output:** `ajuste_sistemico` — um ajuste sistêmico concreto e único

---

### Step 4: Celebrar Progresso

**Ação:**
- Identificar 1-3 vitórias da semana (por menores que sejam)
- Reconhecer o progresso cumulativo: "Cada hábito executado é um voto pela identidade"
- Lembrar: "O platô do potencial latente — o trabalho se acumula mesmo quando os resultados ainda não aparecem"
- Reforçar identidade: "Que tipo de pessoa você foi esta semana?"

**Output:** `celebracoes` — lista de vitórias reconhecidas + afirmação de identidade

---

### Step 5: Planejar a Próxima Semana

**Ação:**
- Definir intenção da próxima semana (não lista de tarefas — orientação de identidade)
- Confirmar quais hábitos manter, ajustar ou pausar
- Aplicar o único ajuste sistêmico definido no Step 3
- Lembrar a regra "nunca falhe duas vezes" para a próxima semana

**Output:** `intencao_proxima_semana` — orientação de identidade + hábitos confirmados + ajuste aplicado

---

## Veto Conditions

| Condição | Ação | Razão |
|----------|------|-------|
| Lição aprendida é motivacional (não sistêmica) | REFORMULAR — exigir termos de sistema | Lições motivacionais não geram mudanças duráveis |
| Mais de um ajuste sistêmico proposto | PRIORIZAR — escolher apenas um | Múltiplos ajustes impossibilitam identificar causa de mudança |
| Celebração ignorada ou pulada | VETO — celebração não é opcional | Recompensa emocional positiva sustenta o loop de hábito |

---

## Output Format

Estrutura do relatório:
1. **Consistência da Semana** — scorecard por hábito
2. **Lição Aprendida** — insight sistêmico
3. **Ajuste para Próxima Semana** — ação concreta única
4. **Vitórias Celebradas** — progresso reconhecido
5. **Intenção da Próxima Semana** — orientação de identidade

---

## Completion Criteria

- [ ] Consistência de cada hábito calculada e classificada
- [ ] Uma lição sistêmica formulada (não motivacional)
- [ ] Exatamente um ajuste sistêmico definido para próxima semana
- [ ] Mínimo uma vitória celebrada
- [ ] Intenção da próxima semana declarada em termos de identidade
- [ ] Regra "nunca falhe duas vezes" reforçada

---

*Task Version: 1.0 — 2026-05-29*
