# Task: Revisar Hábitos

**Task ID:** revisar-habitos
**Version:** 1.0
**Purpose:** Auditar hábitos atuais usando o Habits Scorecard — identificar o que manter, adaptar ou eliminar
**Agent:** assistente-pessoal (Clara)
**Mode:** Interactive

---

## Inputs

| Parâmetro | Tipo | Obrigatório | Descrição |
|-----------|------|-------------|-----------|
| `lista_habitos` | list | Não | Lista de hábitos atuais (se disponível) |
| `identidade_alvo` | string | Não | Quem o usuário quer se tornar |
| `periodo_revisao` | string | Não | Período analisado (última semana, mês, etc.) |

---

## Steps

### Step 1: Listar Todos os Hábitos Atuais

**Ação:**
- Solicitar lista completa de comportamentos habituais (bons e ruins)
- Se usuário não tem lista: guiar descoberta por rotina (manhã → tarde → noite)
- Incluir: hábitos de saúde, trabalho, relacionamentos, consumo de mídia, alimentação
- Meta: identificar todos os hábitos, não apenas os positivos

**Output:** `lista_habitos_completa` — lista de todos os hábitos identificados

---

### Step 2: Aplicar o Habits Scorecard

**Ação:**
- Para cada hábito, classificar com:
  - **(+)** Hábito que serve à identidade desejada e metas
  - **(=)** Hábito neutro (nem ajuda nem prejudica)
  - **(-)** Hábito que contradiz a identidade desejada
- Perguntar guia para cada hábito: "Esse comportamento serve à pessoa que quero me tornar?"
- Lembrar: não é julgamento moral — é análise de alinhamento com identidade

**Output:** `scorecard_habitos` — lista anotada com classificação +/=/−

**Veto condition:**
- Se usuário recusa classificar hábitos negativos → explorar resistência antes de prosseguir

---

### Step 3: Diagnosticar Hábitos Problemáticos por Lei

**Ação:**
- Para cada hábito (+) com baixa consistência, identificar qual Lei está falhando:
  - Cue não óbvio? → Lei 1 quebrada
  - Não é atrativo o suficiente? → Lei 2 quebrada
  - Muito difícil/alto esforço? → Lei 3 quebrada
  - Sem satisfação imediata? → Lei 4 quebrada
- Para cada hábito (−), mapear como as 4 Leis invertidas o sustentam:
  - Muito óbvio? → tornar invisível
  - Muito atrativo? → tornar não atrativo
  - Muito fácil? → adicionar fricção
  - Muito satisfatório imediatamente? → remover recompensa imediata

**Output:** `diagnostico_por_lei` — causa raiz de cada hábito problemático

---

### Step 4: Priorizar Intervenções

**Ação:**
- Selecionar os 3 hábitos mais impactantes para intervenção:
  - 1 hábito (+) com baixa consistência para fortalecer
  - 1 hábito (−) de alto impacto para enfraquecer
  - 1 hábito (=) que pode ser substituído por (+)
- Para cada um: definir uma ação sistêmica concreta (não motivacional)

**Output:** `plano_intervencao` — 3 intervenções priorizadas com ações concretas

---

### Step 5: Gerar Relatório de Auditoria

**Ação:**
- Compilar scorecard, diagnóstico e plano em relatório estruturado
- Incluir: taxa geral de (+) vs (−), principais gargalos sistêmicos, próximos passos
- Lembrar ao usuário: mudança de ambiente antes de mudança de comportamento

**Output:** Relatório de auditoria apresentado ao usuário

---

## Veto Conditions

| Condição | Ação | Razão |
|----------|------|-------|
| Lista de hábitos vazia | VETO — listar antes de auditar | Não há como auditar o que não foi mapeado |
| Diagnóstico sem causa raiz da Lei | VETO — identificar Lei quebrada especificamente | Solução genérica não resolve problema específico |
| Plano de intervenção motivacional (não sistêmico) | REFORMULAR — exigir mudança de ambiente ou sinal | Motivação não é sistema, não escala |

---

## Output Format

Referência: relatório gerado inline com seções: Scorecard | Diagnóstico | Plano de Intervenção

---

## Completion Criteria

- [ ] Todos os hábitos atuais listados (mínimo 5)
- [ ] Scorecard completo com classificação +/=/− para cada hábito
- [ ] Causa raiz identificada por Lei para hábitos problemáticos
- [ ] 3 intervenções priorizadas com ações sistêmicas concretas
- [ ] Relatório apresentado com próximos passos

---

*Task Version: 1.0 — 2026-05-29*
