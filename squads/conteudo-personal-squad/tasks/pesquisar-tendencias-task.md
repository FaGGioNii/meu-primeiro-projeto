# Task: Pesquisar Tendências

**Task ID:** pesquisar-tendencias
**Version:** 1.0
**Purpose:** Identificar temas com alto potencial de engajamento para o público do Faggioni Personal Studio
**Agent:** pesquisador-tendencias (Iris)
**Mode:** Interactive

---

## Inputs

| Parâmetro | Tipo | Obrigatório | Descrição |
|-----------|------|-------------|-----------|
| `periodo` | string | Não | "semana", "quinzena" ou data específica (padrão: semana atual) |
| `area_foco` | string | Não | "treino", "nutrição", "mental", "rotina" ou "todos" (padrão: todos) |
| `formato_prioritario` | string | Não | "reels", "carrossel", "story", "whatsapp" ou "todos" |

---

## Steps

### Step 1: Definir Escopo da Pesquisa

**Ação:**
- Confirmar período (semana atual se não informado)
- Confirmar área de foco
- Verificar se há datas comemorativas ou eventos fitness relevantes no período
  - Exemplos: Dia Mundial da Saúde, início de verão, virada do ano, Dia das Mães
- Registrar contexto sazonal

**Output:** `escopo_pesquisa` — período, área, contexto sazonal

---

### Step 2: Mapear Temas Evergreen do Nicho

**Ação:**
- Selecionar 2-3 temas atemporais do banco abaixo que se encaixam na área de foco:

**Banco de Temas Evergreen — Personal Trainer Online:**

*Treino:*
- Treino em casa sem equipamento (objeção principal do público)
- Por que treinar 3x supera 1x intensa
- Aquecimento: o passo que todo mundo pula
- Progressão de carga: o segredo que ninguém fala
- Erros comuns no agachamento / stiff / remada
- Como montar uma semana de treino equilibrada
- Treino para quem nunca fez academia
- A diferença entre treino personalizado e planilha genérica

*Nutrição:*
- Quanto de proteína você realmente precisa
- Comer de 3 em 3 horas: mito ou necessidade?
- Déficit calórico sem passar fome
- O que comer antes e depois do treino em casa
- Por que a balança mente (mas o espelho não)
- Hidratação e performance — o básico que funciona

*Mentalidade/Rotina:*
- Consistência vs perfeição: o que gera resultado
- Como encaixar treino na rotina de quem trabalha muito
- O que fazer quando bate a preguiça
- Por que você começa e para (e como resolver)
- Resultado visível: quanto tempo realmente leva
- Comparar evolução com você mesmo, não com outras pessoas

**Output:** `temas_evergreen_selecionados` — 2-3 temas com justificativa

---

### Step 3: Identificar Temas de Tendência Atual

**Ação:**
- Com base no contexto sazonal (Step 1), identificar 1-2 temas com tração atual:
  - Jan/Fev: "Ano novo, começar do zero" — rotina, metas, consistência
  - Mar/Abr: Páscoa — culpa x liberdade, chocolate sem culpa
  - Mai/Jun: Dia das Mães, aproximação do inverno — treino no frio, presente
  - Jul/Ago: Meio do ano — revisão de metas, onde você está
  - Set/Out: Aproximação do verão — urgência, resultado, antes e depois
  - Nov/Dez: Festas — como não perder tudo, manutenção, presentes

**Output:** `temas_tendencia` — 1-2 temas sazonais com ângulo específico

---

### Step 4: Definir Ângulos e Formatos

**Ação:**
Para cada tema selecionado (Steps 2 e 3), definir:
- **Ângulo principal:** por que este tema engaja AGORA para este público
- **Formato recomendado:** Reels / Carrossel / Foto / Story / WhatsApp
- **Gancho sugerido:** frase de abertura testada para o público
- **Palavras-chave/hashtags:** 5-10 por tema
- **Nível de esforço de criação:** baixo / médio / alto

**Critérios de seleção de ângulo:**
- O ângulo nomeia uma dor ou desejo real do público?
- É diferente do que outros personal trainers estão fazendo?
- Posiciona o Hendrew como autoridade prática (não teórica)?

**Output:** `temas_com_angulos` — briefing completo por tema

---

### Step 5: Montar Briefing de Tendências

**Ação:**
- Consolidar todos os temas em briefing estruturado
- Priorizar: 1 tema de alta urgência + 2-3 temas de alto valor
- Incluir sugestão de distribuição semanal
- Passar briefing para @redator-conteudo

**Output:** Briefing completo pronto para o redator

---

## Veto Conditions

| Condição | Ação | Razão |
|----------|------|-------|
| Tema muito técnico para o público | REJEITAR — substituir por versão acessível | Público não é especialista em fitness |
| Tendência apenas fora do Brasil | REJEITAR — só incluir se já chegou ao BR | Contexto brasileiro é prioridade |
| Mais de 5 temas no briefing | FILTRAR — escolher os mais relevantes | Foco é mais eficaz que volume |

---

## Output Format

```markdown
## Briefing de Tendências — [Período]

### Contexto Sazonal
[Épocas, datas, eventos relevantes]

### Tema 1: [Nome] — ALTA PRIORIDADE
- **Ângulo:** [Por que este ângulo agora]
- **Formato sugerido:** [Reels / Carrossel / Story / WhatsApp]
- **Gancho:** "[Frase de abertura sugerida]"
- **Hashtags:** #tag1 #tag2 #tag3 #tag4 #tag5
- **Esforço de criação:** [Baixo / Médio / Alto]

### Tema 2: [Nome]
[mesma estrutura]

### Tema 3: [Nome]
[mesma estrutura]

### Sugestão de Distribuição Semanal
- Segunda: [Tema X] — [Formato]
- Quarta: [Tema Y] — [Formato]
- Sexta: [Tema Z] — [Formato]
- WhatsApp: [quando e o quê]
```

---

## Completion Criteria

- [ ] Contexto sazonal mapeado
- [ ] Mínimo 1 tema evergreen selecionado com ângulo específico
- [ ] Mínimo 1 tema de tendência atual identificado
- [ ] Todos os temas têm gancho sugerido e hashtags
- [ ] Briefing consolidado e pronto para @redator-conteudo

---

*Task Version: 1.0 — 2026-05-30*
