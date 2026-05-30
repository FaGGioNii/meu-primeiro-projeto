# Task: Criar Hábito

**Task ID:** criar-habito
**Version:** 1.0
**Purpose:** Criar novo hábito usando as 4 Leis da Mudança de Comportamento (Atomic Habits — James Clear)
**Agent:** assistente-pessoal (Clara)
**Mode:** Interactive

---

## Inputs

| Parâmetro | Tipo | Obrigatório | Descrição |
|-----------|------|-------------|-----------|
| `habito_desejado` | string | Sim | Comportamento que o usuário quer incorporar |
| `frequencia_alvo` | string | Não | Frequência desejada (diário, 3x/semana, etc.) |
| `habito_ancora` | string | Não | Hábito existente para empilhamento |

---

## Steps

### Step 1: Declarar Identidade Alvo

**Ação:**
- Perguntar: "Que tipo de pessoa faz esse hábito naturalmente?"
- Reformular o hábito como declaração de identidade: "Eu sou uma pessoa que..."
- Confirmar que a identidade ressoa com o usuário
- Exemplo: hábito = "ler 20 min/dia" → identidade = "Sou uma pessoa curiosa que aprende continuamente"

**Output:** `identidade_alvo` — declaração de identidade no formato "Sou uma pessoa que..."

**Veto condition:**
- Se usuário resistir à declaração de identidade → explorar o porquê antes de prosseguir

---

### Step 2: Aplicar Lei 1 — Tornar Óbvio (Cue)

**Ação:**
- Identificar ou criar sinal visual/temporal para o hábito
- Opções de sinal:
  - **Temporal:** horário específico ("às 7h")
  - **Visual:** objeto no ambiente ("tênis ao lado da cama")
  - **Empilhamento:** hábito âncora existente ("depois do café")
- Definir declaração de implementação de intenção: "Quando [SINAL], farei [HÁBITO] em [LOCAL]"
- Verificar se o sinal é óbvio o suficiente no ambiente atual

**Output:** `lei1_cue` — sinal definido + declaração de implementação

---

### Step 3: Aplicar Lei 2 — Tornar Atrativo (Craving)

**Ação:**
- Identificar o que torna o hábito atrativo OU criar atração:
  - **Temptation bundling:** "Só posso fazer X (prazer) depois/durante Y (hábito)"
  - **Reformulação:** "Eu tenho que..." → "Eu consigo...", "Isso me permite..."
  - **Associação positiva:** conectar hábito à identidade desejada
- Definir estratégia de atração concreta

**Output:** `lei2_craving` — estratégia de atração definida

---

### Step 4: Aplicar Lei 3 — Tornar Fácil (Response)

**Ação:**
- Aplicar a Regra de 2 Minutos: reduzir hábito à versão mínima executável em 2 min
  - Exemplo: "fazer exercício 1h" → "calçar tênis e sair pela porta"
  - Exemplo: "meditar 20 min" → "sentar, fechar os olhos por 2 min"
- Identificar e eliminar fontes de fricção:
  - Preparação antecipada (o que colocar na frente?)
  - O que remover do caminho?
  - Como reduzir número de passos até o hábito?
- Definir ambiente preparado para o hábito

**Output:** `lei3_response` — versão de 2 minutos + ações de redução de fricção

---

### Step 5: Aplicar Lei 4 — Tornar Satisfatório (Reward)

**Ação:**
- Definir recompensa imediata que ocorre LOGO após o hábito
- Opções:
  - **Hábito tracker:** marcar X na corrente (satisfação visual)
  - **Micro-celebração:** gesto/palavra de celebração interna
  - **Recompensa tangível:** pequeno prazer imediato vinculado ao hábito
- Regra: a recompensa deve ocorrer dentro de 60 segundos após o comportamento
- Verificar alinhamento com identidade (recompensa não deve contradizer identidade)

**Output:** `lei4_reward` — recompensa imediata definida

**Veto condition:**
- Se recompensa contradiz a identidade (ex: comer doce após exercício) → reformular

---

### Step 6: Montar Especificação Completa do Hábito

**Ação:**
- Compilar todas as 4 Leis em template `templates/habito-novo-tmpl.md`
- Incluir: identidade, cue, craving, response (versão 2 min), reward
- Adicionar empilhamento de hábitos se âncora foi identificada
- Definir sistema de rastreamento (app, papel, calendário)
- Lembrar: "Nunca falhe duas vezes — se quebrar a corrente, retome no dia seguinte"

**Output:** Especificação completa do hábito apresentada ao usuário

---

## Veto Conditions

| Condição | Ação | Razão |
|----------|------|-------|
| Nenhuma identidade definida | VETO — identidade é fundação do hábito | Hábito sem identidade tem baixa durabilidade |
| Hábito sem sinal claro | VETO — definir cue antes de prosseguir | Comportamento precisa de trigger para ativar |
| Versão 2 min não definida | VETO — escalar é mais fácil que começar | Regra de 2 min reduz barreira de início |
| Recompensa imediata ausente | VETO — satisfação imediata é essencial | Cérebro aprende por recompensa imediata, não futura |
| Recompensa contradiz identidade | REFORMULAR — alinhar recompensa e identidade | Inconsistência enfraquece o loop de hábito |

---

## Output Format

Referência: `templates/habito-novo-tmpl.md`

---

## Completion Criteria

- [ ] Identidade alvo declarada no formato "Sou uma pessoa que..."
- [ ] Lei 1 (Cue): sinal específico + declaração de implementação
- [ ] Lei 2 (Craving): estratégia de atração concreta
- [ ] Lei 3 (Response): versão de 2 minutos definida + fricção reduzida
- [ ] Lei 4 (Reward): recompensa imediata alinhada com identidade
- [ ] Empilhamento definido (se hábito âncora disponível)
- [ ] Sistema de rastreamento escolhido

---

*Task Version: 1.0 — 2026-05-29*
