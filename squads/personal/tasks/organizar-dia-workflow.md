# Task: Organizar Dia

**Task ID:** organizar-dia
**Version:** 1.0
**Purpose:** Organizar o dia usando sistemas de hábitos, blocos de tempo e momentos decisivos (Atomic Habits)
**Agent:** assistente-pessoal (Clara)
**Mode:** Interactive

---

## Inputs

| Parâmetro | Tipo | Obrigatório | Descrição |
|-----------|------|-------------|-----------|
| `contexto_dia` | string | Não | Contexto especial do dia (reuniões, compromissos, energia) |
| `prioridades` | list | Não | Lista de tarefas/metas do dia |
| `hábitos_ativos` | list | Não | Hábitos que o usuário já pratica |

---

## Steps

### Step 1: Identificar Hábito Âncora da Manhã

**Ação:**
- Perguntar: "Qual é sua primeira ação consistente ao acordar?" (ex: café, banho, alarme)
- Identificar hábito âncora sólido existente
- Confirmar consistência (>80% dos dias)

**Output:** `habito_ancora_manha` — hábito âncora identificado

**Veto condition:**
- Se não há hábito âncora consistente → sugerir criar um antes de organizar o dia

---

### Step 2: Mapear 3 Prioridades do Dia

**Ação:**
- Solicitar lista de tarefas/compromissos do dia
- Aplicar filtro de identidade: "Qual tarefa, se feita, avança quem você quer se tornar?"
- Selecionar e ordenar 3 prioridades por impacto sistêmico (não urgência)
- Identificar a tarefa MIT (Most Important Task) — deve ser feita antes do almoço

**Output:** `prioridades_ordenadas` — lista de 3 tarefas com justificativa sistêmica

**Veto condition:**
- Se lista tem mais de 10 itens sem filtro → forçar filtro de identidade antes de prosseguir

---

### Step 3: Estruturar Blocos de Tempo

**Ação:**
- Criar estrutura de 3 blocos usando hábitos âncora como divisores:
  - **Bloco Manhã** (âncora: acordar → antes do almoço): MIT + hábitos de alta energia
  - **Bloco Tarde** (âncora: almoço → antes do jantar): Trabalho de foco + reuniões
  - **Bloco Noite** (âncora: jantar → dormir): Revisão + preparação + relaxamento
- Alocar prioridades nos blocos conforme energia natural do usuário
- Inserir pausas obrigatórias (reduz fricção cognitiva)

**Output:** `estrutura_blocos` — 3 blocos com tarefas alocadas

---

### Step 4: Identificar Momentos Decisivos

**Ação:**
- Mapear 3-5 "momentos decisivos" do dia: pequenas escolhas de alto impacto
  - Exemplos: "Ao acordar, calço o tênis antes de olhar o celular"
  - "Antes de abrir e-mail, completo a MIT do dia"
  - "Depois do almoço, 10 min de caminhada antes de retornar ao trabalho"
- Cada momento decisivo deve ter formato: "Quando [situação], farei [ação]"

**Output:** `momentos_decisivos` — lista de 3-5 declarações de implementação de intenção

**Veto condition:**
- Se momento decisivo não tem trigger claro → reformular com "Quando X, farei Y"

---

### Step 5: Gerar Plano do Dia

**Ação:**
- Compilar tudo no template `templates/plano-dia-tmpl.md`
- Incluir: hábito âncora, 3 prioridades (MIT destacada), blocos, momentos decisivos
- Adicionar lembrete do sistema: "Nunca falhe duas vezes"

**Output:** Plano do dia preenchido e apresentado ao usuário

---

## Veto Conditions

| Condição | Ação | Razão |
|----------|------|-------|
| Nenhum hábito âncora identificado | VETO — criar hábito âncora primeiro | Sem âncora, o empilhamento não funciona |
| Mais de 5 prioridades sem filtro | VETO — aplicar filtro de identidade | Sistema sobrecarregado falha consistentemente |
| Momento decisivo sem trigger | REFORMULAR — exigir formato "Quando X, farei Y" | Implementação de intenção requer trigger específico |

---

## Output Format

Referência: `templates/plano-dia-tmpl.md`

---

## Completion Criteria

- [ ] Hábito âncora da manhã identificado e confirmado
- [ ] Exatamente 3 prioridades definidas com MIT clara
- [ ] 3 blocos de tempo estruturados com âncoras
- [ ] Mínimo 3 momentos decisivos no formato "Quando X, farei Y"
- [ ] Plano exportado em template

---

*Task Version: 1.0 — 2026-05-29*
