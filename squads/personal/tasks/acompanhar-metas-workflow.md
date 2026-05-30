# Task: Acompanhar Metas

**Task ID:** acompanhar-metas
**Version:** 1.0
**Purpose:** Revisar progresso de metas pessoais e profissionais com foco em sistemas de suporte (não apenas resultados)
**Agent:** assistente-pessoal (Clara)
**Mode:** Interactive

---

## Inputs

| Parâmetro | Tipo | Obrigatório | Descrição |
|-----------|------|-------------|-----------|
| `lista_metas` | list | Sim | Metas ativas do usuário |
| `periodo` | string | Não | Período de revisão (semana, mês, trimestre) |
| `habitos_associados` | map | Não | Hábitos associados a cada meta |

---

## Steps

### Step 1: Inventariar Metas Ativas

**Ação:**
- Listar todas as metas ativas do usuário
- Para cada meta, capturar:
  - O resultado desejado (meta em si)
  - O sistema de hábitos associado (ou ausência dele)
  - Prazo ou horizonte temporal
- Identificar metas sem sistema de suporte → estas são as mais vulneráveis

**Output:** `inventario_metas` — lista de metas com sistemas associados

**Veto condition:**
- Se meta não tem sistema de hábitos associado → antes de prosseguir, definir pelo menos 1 hábito de suporte

---

### Step 2: Avaliar Progresso por Sistema (não por resultado)

**Ação:**
- Para cada meta, avaliar o sistema — não apenas o resultado:
  - "Você executou os hábitos de suporte com qual consistência?" (escala 0-100%)
  - "O sistema teve fricção ou obstáculos?" (o que atrapalhou?)
  - "O sistema produziu os comportamentos esperados?"
- Lembrar: "Você não sobe ao nível das suas metas; você cai ao nível dos seus sistemas"
- Separar avaliação de processo (sistemas) de avaliação de resultado

**Output:** `avaliacao_sistemas` — consistência e qualidade dos sistemas por meta

---

### Step 3: Identificar Ajustes Sistêmicos

**Ação:**
- Para metas com baixa consistência nos sistemas:
  - Diagnosticar gargalo (qual das 4 Leis está falhando?)
  - Propor ajuste sistêmico específico (não motivacional)
- Para metas com boa consistência mas resultado ainda ausente:
  - Identificar se está no "platô do potencial latente" → continuar sistema
  - Verificar se o sistema realmente apoia a meta ou está desalinhado
- Para metas em progresso: identificar o que replicar

**Output:** `ajustes_sistemicos` — mudanças concretas nos sistemas (não nas metas)

---

### Step 4: Priorizar Atenção

**Ação:**
- Classificar metas em 3 categorias:
  - **Manter:** sistema funcionando, consistência alta → apenas registrar
  - **Ajustar:** sistema com gargalo identificado → intervenção sistêmica
  - **Rever:** meta pode não ser mais relevante ou precisa ser reformulada
- Definir 1-2 ações prioritárias para a próxima semana

**Output:** `metas_priorizadas` — classificação + próximas ações

---

### Step 5: Gerar Dashboard de Metas

**Ação:**
- Compilar em template `templates/relatorio-metas-tmpl.md`
- Incluir: inventário, avaliação de sistemas, ajustes, próximas ações
- Destacar: o que está funcionando (para replicar) e o que precisa de ajuste sistêmico

**Output:** Dashboard de metas apresentado ao usuário

---

## Veto Conditions

| Condição | Ação | Razão |
|----------|------|-------|
| Meta sem sistema de hábitos | VETO — definir sistema antes de acompanhar | Sem sistema, a meta é apenas um desejo |
| Avaliação focada apenas em resultados | REFORMULAR — exigir avaliação de processo | Resultados são lagging indicators; sistemas são leading |
| Ajuste motivacional proposto (não sistêmico) | REFORMULAR — especificar mudança de ambiente/sinal | Motivação não é sistema replicável |

---

## Output Format

Referência: `templates/relatorio-metas-tmpl.md`

---

## Completion Criteria

- [ ] Todas as metas ativas listadas com sistemas associados
- [ ] Consistência dos sistemas avaliada (% de execução)
- [ ] Gargalos sistêmicos identificados por Lei
- [ ] Ajustes sistêmicos concretos definidos (não motivacionais)
- [ ] Metas classificadas em Manter/Ajustar/Rever
- [ ] 1-2 ações prioritárias para próxima semana definidas

---

*Task Version: 1.0 — 2026-05-29*
