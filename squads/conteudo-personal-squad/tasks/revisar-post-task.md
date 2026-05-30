# Task: Revisar Post

**Task ID:** revisar-post
**Version:** 1.0
**Purpose:** Revisar conteúdo criado pelo @redator-conteudo garantindo adequação ao público-alvo
**Agent:** revisor-publico (Maya)
**Mode:** Interactive

---

## Inputs

| Parâmetro | Tipo | Obrigatório | Descrição |
|-----------|------|-------------|-----------|
| `conteudo` | string | Sim | Post ou mensagem a revisar (texto completo) |
| `formato` | string | Sim | "reels", "carrossel", "foto", "story", "whatsapp-broadcast", "whatsapp-individual" |
| `objetivo` | string | Não | "lead", "engajamento", "salvar", "autoridade" (padrão: lead) |

---

## Contexto Fixo — Público-Alvo

**Quem vai ler este conteúdo:**
- Adultos com rotina ocupada (trabalhadores, pais/mães)
- Treinam ou querem treinar em casa — sem acesso fácil a academia
- Algum ceticismo: já foram "prometidos" resultados que não vieram
- Nível de conhecimento fitness: básico a intermediário — nada muito técnico
- Objetivo: resultado real e sustentável, não transformação milagrosa
- Decisão de compra: emocional (identificação com o Hendrew) + racional (preço justo, R$ 99,90)

---

## Steps

### Step 1: Leitura como Público

**Ação:**
- Ler o conteúdo integralmente como se fosse um aluno potencial (não como criador)
- Registrar a primeira impressão:
  - "Para ou não para meu scroll?"
  - "Entendo do que se trata nos primeiros 5 segundos?"
  - "Sinto que é para mim ou para outro público?"

**Output:** `primeira_impressao` — percepção inicial do público

---

### Step 2: Aplicar Checklist de 8 Pontos

**Ação:**
Avaliar cada critério com: ✅ PASSA | ⚠️ AJUSTAR | ❌ FALHA

| # | Critério | Verificação |
|---|----------|-------------|
| 1 | **Gancho** | Para o scroll? Nomeia dor ou promessa específica nos primeiros 2-3 segundos? |
| 2 | **Linguagem** | Qualquer adulto sem conhecimento técnico entende 100% do texto? |
| 3 | **Tom** | Soa como o Hendrew falando, não como empresa ou IA? |
| 4 | **Dor/Desejo** | Menciona uma dor real ou desejo concreto do público? |
| 5 | **Credibilidade** | Tem dado, exemplo ou resultado tangível (sem exagero)? |
| 6 | **CTA** | A ação pedida está clara? É de baixo atrito para o estágio atual? |
| 7 | **Formato** | O tamanho e estrutura são adequados para o formato informado? |
| 8 | **Autenticidade** | Livre de "marketeirês", promessas impossíveis ou linguagem performática? |

**Output:** `checklist_resultado` — tabela com resultado de cada critério

---

### Step 3: Identificar Pontos Fortes e Problemas

**Ação:**
- Listar 2-3 pontos fortes específicos (o que funciona bem e por quê)
- Listar cada ⚠️ e ❌ com:
  - O problema específico (citar trecho exato)
  - Por que impacta negativamente no público
  - Sugestão concreta de correção (sempre incluir)

**Veto condition:** Nunca apontar problema sem dar sugestão — isso trava o processo sem gerar valor

**Output:** `pontos_fortes` + `problemas_com_sugestoes`

---

### Step 4: Emitir Veredicto

**Ação:**
Emitir um dos três veredictos com base no checklist:

| Veredicto | Critério | Ação |
|-----------|---------|------|
| **✅ APROVADO** | Todos os 8 critérios ✅ ou no máximo 1 ⚠️ menor | Conteúdo pronto para publicar como está |
| **⚠️ AJUSTAR** | 1-3 critérios ⚠️, nenhum ❌ | Aplicar ajustes pontuais e aprovar sem nova rodada |
| **❌ REESCREVER** | Qualquer ❌ ou 4+ critérios ⚠️ | Devolver para @redator-conteudo com feedback completo |

Se veredicto for **AJUSTAR**: aplicar os ajustes diretamente e entregar versão corrigida.
Se veredicto for **REESCREVER**: entregar briefing de reescrita claro para o redator.

**Output:** `veredicto` + versão final (se APROVADO ou AJUSTAR) ou briefing de reescrita (se REESCREVER)

---

## Veto Conditions

| Condição | Ação | Razão |
|----------|------|-------|
| CTA ausente | REESCREVER automaticamente — não negociar | Todo conteúdo precisa de ação clara |
| Promessa impossível (ex: "elimine 10kg em 1 mês") | REESCREVER — substituir por resultado realista | Gera desconfiança no público cético |
| Linguagem que o Hendrew jamais usaria | AJUSTAR tom antes de aprovar | Quebra autenticidade que é o principal diferencial |
| Jargão técnico sem tradução | AJUSTAR — simplificar a linguagem | Público não é especialista |

---

## Output Format

```markdown
## REVISÃO — [Formato] — [Tema]

### Primeira Impressão (perspectiva do público)
[2-3 linhas sobre a experiência de leitura como aluno potencial]

### Checklist de Qualidade

| # | Critério | Resultado | Nota |
|---|----------|-----------|------|
| 1 | Gancho | ✅/⚠️/❌ | [breve nota] |
| 2 | Linguagem | ✅/⚠️/❌ | [breve nota] |
| 3 | Tom | ✅/⚠️/❌ | [breve nota] |
| 4 | Dor/Desejo | ✅/⚠️/❌ | [breve nota] |
| 5 | Credibilidade | ✅/⚠️/❌ | [breve nota] |
| 6 | CTA | ✅/⚠️/❌ | [breve nota] |
| 7 | Formato | ✅/⚠️/❌ | [breve nota] |
| 8 | Autenticidade | ✅/⚠️/❌ | [breve nota] |

### Pontos Fortes
- [ponto 1 específico com citação do texto]
- [ponto 2]

### Ajustes Necessários
- ⚠️ [Trecho problemático] → Sugestão: [trecho alternativo] — Motivo: [por quê]
- (se houver mais)

### VEREDICTO: [✅ APROVADO / ⚠️ AJUSTAR / ❌ REESCREVER]

[Se APROVADO ou AJUSTAR]
**Versão Final:**
---
[conteúdo final aprovado completo]
---

[Se REESCREVER]
**Briefing para @redator-conteudo:**
- Problema principal: [descrever]
- O que reescrever: [especificar]
- Manter: [o que estava certo]
- Mudar: [o que precisa mudar + sugestões]
```

---

## Completion Criteria

- [ ] Leitura completa como público-alvo realizada
- [ ] Checklist de 8 pontos preenchido com justificativas
- [ ] Pontos fortes identificados (mínimo 2)
- [ ] Cada problema tem sugestão concreta
- [ ] Veredicto emitido com clareza
- [ ] Versão final entregue (APROVADO/AJUSTAR) ou briefing de reescrita (REESCREVER)

---

*Task Version: 1.0 — 2026-05-30*
