# Workflow: Pipeline de Conteúdo Semanal

**Workflow ID:** pipeline-conteudo-semanal
**Version:** 1.0
**Purpose:** Orquestrar os 3 agentes do squad para produzir conteúdo pronto para publicar
**Modo:** Interactive

---

## Visão Geral

```
@pesquisador-tendencias        @redator-conteudo           @revisor-publico
       │                              │                            │
       ▼                              ▼                            ▼
*pesquisar-tendencias  →    *criar-post (por tema)   →    *revisar (cada post)
       │                              │                            │
  Briefing com                  Rascunho do                  APROVADO /
  temas e ângulos               conteúdo                    AJUSTAR /
                                                             REESCREVER
                                                                  │
                                                           Conteúdo final
                                                         pronto para publicar
```

---

## Fases

### Fase 1: Briefing (Iris — @pesquisador-tendencias)

**Duração estimada:** 10-15 minutos
**Comando:** `*pesquisar-tendencias` ou `*briefing-semanal`

**O que acontece:**
- Iris mapeia contexto sazonal da semana
- Seleciona 2-3 temas evergreen + 1 tema de tendência atual
- Define ângulo, formato recomendado e gancho sugerido para cada tema
- Entrega briefing estruturado

**Entregável:**
```
Briefing de Tendências com:
- 3-4 temas priorizados
- Ângulo específico por tema
- Formato sugerido (Reels / Carrossel / WhatsApp)
- Gancho de abertura para cada tema
- Hashtags por tema
```

**Próximo:** Passar briefing para @redator-conteudo

---

### Fase 2: Criação (Leo — @redator-conteudo)

**Duração estimada:** 10-20 minutos por post
**Comando:** `*criar-post [tema]` ou `*criar-mensagem [objetivo]`

**O que acontece:**
- Leo recebe briefing com tema e ângulo
- Escreve gancho, corpo e CTA no formato solicitado
- Seleciona hashtags em 3 camadas (para Instagram)
- Verifica voz e tom antes de entregar

**Entregável:**
- Post completo (legenda + hashtags) — Instagram
- Mensagem completa — WhatsApp
- Slides com textos — Carrossel

**Próximo:** Passar rascunho para @revisor-publico

---

### Fase 3: Revisão (Maya — @revisor-publico)

**Duração estimada:** 5-10 minutos por post
**Comando:** `*revisar [conteúdo]`

**O que acontece:**
- Maya lê o conteúdo como aluno potencial
- Aplica checklist de 8 pontos
- Emite veredicto: APROVADO / AJUSTAR / REESCREVER

**Entregável:**
- Se APROVADO: conteúdo pronto para publicar
- Se AJUSTAR: versão corrigida pronto para publicar
- Se REESCREVER: briefing para @redator-conteudo com feedback

**Se REESCREVER:** Volta para Fase 2 → Leo reescreve → Fase 3 novamente (máx 2 rodadas)

---

### Fase 4: Conteúdo Pronto

**O Hendrew recebe:**
- Posts aprovados, formatados, prontos para copiar e publicar
- Notas de uso: melhor horário, dica de arte (se relevante)
- CTA já incluído — não precisa adaptar

---

## Fluxo Decisório

```
Veredicto Maya
    │
    ├─ APROVADO → ✅ Conteúdo pronto para publicar
    │
    ├─ AJUSTAR  → Maya aplica ajuste → ✅ Conteúdo pronto
    │
    └─ REESCREVER
           │
           ├─ Iteração 1: Leo reescreve → Maya revisa novamente
           │
           └─ Iteração 2 (se necessário): Leo reescreve → Maya revisa
                  │
                  └─ Se ainda REESCREVER após 2 rodadas → Hendrew decide
```

---

## Modo Rápido (quando não há tempo para pipeline completo)

Se não houver tempo para a Fase 1:
1. Ir direto para Leo com tema em mãos: `*criar-post [tema específico]`
2. Leo cria, Maya revisa
3. Pular Iris e usar um dos temas evergreen do banco de temas

---

## Cadência Sugerida de Publicação

| Dia | Canal | Formato | Observação |
|-----|-------|---------|------------|
| Segunda | Instagram | Reels ou Carrossel | Tema motivacional ou prático |
| Quarta | Instagram | Foto ou Carrossel | Educativo, autoridade |
| Sexta | Instagram | Reels | Engajamento alto no final de semana |
| Qualquer dia | WhatsApp | Broadcast | 1-2x por semana, não mais |

---

## Comandos Rápidos por Fase

**Fase 1 — Briefing:**
- `*pesquisar-tendencias` — tendências da semana
- `*briefing-semanal` — calendário completo 7 dias
- `*temas-evergreen` — banco de temas atemporais

**Fase 2 — Criação:**
- `*criar-post [tema]` — post Instagram
- `*criar-mensagem [objetivo]` — WhatsApp
- `*criar-carrossel [tema]` — carrossel
- `*criar-sequencia [tema]` — 3-7 posts

**Fase 3 — Revisão:**
- `*revisar` — checklist completo
- `*aprovar` — aprovação final
- `*ajustar-tom` — só ajuste de tom sem reescrever

---

*Workflow Version: 1.0 — 2026-05-30*
*Squad: conteudo-personal-squad*
