# Workflow: Gerar Semana Completa de Conteúdo

**Workflow ID:** gerar-semana-completa
**Versão:** 1.0
**Comando:** `*gerar-semana`
**Tempo estimado:** 20–30 minutos
**Output:** 3 posts Instagram + 1 mensagem WhatsApp + calendário de publicação

---

## O que este workflow entrega

```
✅ Post 1 — Reels (engajamento + lead)
✅ Post 2 — Carrossel (autoridade + educação)
✅ Post 3 — Foto ou Story (relacionamento)
✅ Mensagem WhatsApp broadcast (nutrição de lista)
✅ Calendário sugerido (dia e horário de cada publicação)
```

Todos revisados e aprovados pela Maya antes de entregar.

---

## Como executar

Digite `*gerar-semana` em qualquer um dos 3 agentes do squad.
O workflow conduz você por cada etapa automaticamente.

---

## ETAPA 1 — Briefing Semanal (Iris)

**Agente:** `@pesquisador-tendencias`
**Duração:** ~5 min

### Instruções para Iris:

Executar pesquisa completa de tendências e montar briefing com exatamente **4 temas** nesta ordem:

| # | Tema | Formato | Objetivo |
|---|------|---------|---------|
| Tema 1 | Tendência sazonal ou evergreen de alta urgência | **Reels** | Engajamento + lead |
| Tema 2 | Educativo / autoridade (mito, erro comum, dica técnica) | **Carrossel** | Autoridade + salvar |
| Tema 3 | Relacionamento / motivação | **Foto ou Story** | Conexão com audiência |
| Tema 4 | Dica prática / lembrete | **WhatsApp** | Nutrição de lista |

Para cada tema entregar:
- Ângulo específico
- Gancho sugerido (frase de abertura)
- Palavras-chave e hashtags
- Observação sazonal (se houver)

**Output desta etapa:** `BRIEFING_SEMANAL` — salvo na conversa para as próximas etapas

---

## ETAPA 2 — Post 1: Reels (Leo)

**Agente:** `@redator-conteudo`
**Input:** Tema 1 do BRIEFING_SEMANAL
**Duração:** ~5 min

### Instruções para Leo:

Usar o Tema 1 do briefing. Formato Reels. Seguir task `criar-post-task.md`.

**Estrutura obrigatória:**
```
[Gancho — 1-2 linhas]

[Espaço]

[Corpo — 3-5 linhas]

[Espaço]

[CTA direto]

[Espaço]
.
.
.
[Hashtags — bloco separado]
```

**Output desta etapa:** `POST_1_REELS` — rascunho completo

---

## ETAPA 3 — Post 2: Carrossel (Leo)

**Agente:** `@redator-conteudo`
**Input:** Tema 2 do BRIEFING_SEMANAL
**Duração:** ~5 min

### Instruções para Leo:

Usar o Tema 2 do briefing. Formato Carrossel. Seguir task `criar-post-task.md`.

**Estrutura obrigatória:**
```
Slide 0 (Capa): [Promessa ou pergunta — máx 7 palavras]
Slide 1: [Ponto 1 — título curto + 2 linhas]
Slide 2: [Ponto 2 — título curto + 2 linhas]
Slide 3: [Ponto 3 — título curto + 2 linhas]
Slide 4: [Ponto 4 — opcional]
Slide Final: [CTA + "Salva esse post"]

Legenda: [Gancho + 2-3 linhas + CTA + hashtags]
```

Mínimo 4 slides, máximo 8.

**Output desta etapa:** `POST_2_CARROSSEL` — slides + legenda completos

---

## ETAPA 4 — Post 3: Foto ou Story (Leo)

**Agente:** `@redator-conteudo`
**Input:** Tema 3 do BRIEFING_SEMANAL
**Duração:** ~3 min

### Instruções para Leo:

Usar o Tema 3 do briefing. Formato Foto (se tema mais substancial) ou Story com enquete (se tema de relacionamento/interação). Seguir task `criar-post-task.md`.

**Formato Foto:**
```
[Gancho]
[Espaço]
[Corpo 4-6 linhas]
[Espaço]
[CTA engajamento: pergunta ou "comenta aqui"]
[Hashtags]
```

**Formato Story com enquete:**
```
Tela 1: [Pergunta curta + enquete com 2 opções]
Tela 2 (resposta, postar depois): [Revelação + CTA WhatsApp]
```

**Output desta etapa:** `POST_3_FOTO_OU_STORY` — conteúdo completo

---

## ETAPA 5 — Mensagem WhatsApp (Leo)

**Agente:** `@redator-conteudo`
**Input:** Tema 4 do BRIEFING_SEMANAL
**Duração:** ~3 min

### Instruções para Leo:

Usar o Tema 4 do briefing. Formato WhatsApp broadcast. Seguir template `mensagem-whatsapp-tmpl.md`.

**Regras obrigatórias:**
- Máx 120 palavras
- Abertura direta (não "Tudo bem?")
- Uma única ideia
- CTA suave no final

**Output desta etapa:** `MENSAGEM_WHATSAPP` — mensagem completa pronta para copiar

---

## ETAPA 6 — Revisão em Bloco (Maya)

**Agente:** `@revisor-publico`
**Input:** POST_1 + POST_2 + POST_3 + MENSAGEM_WHATSAPP
**Duração:** ~5 min

### Instruções para Maya:

Revisar os 4 conteúdos sequencialmente. Para cada um:
- Aplicar checklist de 8 pontos (versão rápida)
- Emitir veredicto: ✅ APROVADO / ⚠️ AJUSTAR / ❌ REESCREVER
- Se AJUSTAR: aplicar diretamente e entregar versão corrigida
- Se REESCREVER: indicar qual etapa refazer (voltar para Leo)

Apresentar revisão no formato:

```
POST 1 (Reels): ✅ APROVADO / ⚠️ AJUSTAR [o que ajustar]
POST 2 (Carrossel): ✅ APROVADO / ⚠️ AJUSTAR [o que ajustar]
POST 3 (Foto/Story): ✅ APROVADO / ⚠️ AJUSTAR [o que ajustar]
WhatsApp: ✅ APROVADO / ⚠️ AJUSTAR [o que ajustar]
```

**Output desta etapa:** 4 conteúdos aprovados com versões finais

---

## ETAPA 7 — Pacote Semanal Final

Ao final da Etapa 6, entregar tudo consolidado neste formato:

```
═══════════════════════════════════════
📦 PACOTE DE CONTEÚDO — SEMANA [DATA]
═══════════════════════════════════════

📱 POST 1 — REELS
Publicar: [dia sugerido] às [horário]
---
[conteúdo final aprovado]
---

📊 POST 2 — CARROSSEL
Publicar: [dia sugerido] às [horário]
---
[slides + legenda final aprovada]
---

📸 POST 3 — FOTO / STORY
Publicar: [dia sugerido] às [horário]
---
[conteúdo final aprovado]
---

💬 MENSAGEM WHATSAPP
Enviar: [dia sugerido] às [horário]
---
[mensagem final aprovada]
---

📅 CALENDÁRIO DA SEMANA
Segunda:  [Post X] — [formato] — [horário]
Quarta:   [Post X] — [formato] — [horário]
Quinta:   [WhatsApp] — [horário]
Sexta:    [Post X] — [formato] — [horário]

═══════════════════════════════════════
```

---

## Calendário de Publicação Recomendado

| Dia | Horário | Conteúdo | Motivo |
|-----|---------|----------|--------|
| **Segunda** | 19h–21h | Post 1 (Reels) | Início de semana, energia alta |
| **Quarta** | 12h–13h | Post 2 (Carrossel) | Meio da semana, pico de engajamento |
| **Quinta** | 18h–19h | WhatsApp broadcast | Antecede o fim de semana |
| **Sexta** | 18h–20h | Post 3 (Foto/Story) | Tráfego alto, clima descontraído |

---

## Versão Expressa (quando tem pouco tempo)

Se quiser só o essencial:

```
*gerar-semana --express
```

Entrega apenas:
- 1 Reels (tema mais forte da semana)
- 1 mensagem WhatsApp
- Sem carrossel e sem foto
- Tempo: ~10 minutos
```

---

## Observações

- Se um conteúdo for REESCREVER, volte para Leo com o feedback da Maya antes de continuar
- O pacote completo pode ser salvo em `docs/conteudo/semana-[data].md` para referência futura
- Hashtags podem ser reutilizadas entre posts da mesma semana sem problema

---

*Workflow Version: 1.0 — 2026-05-30*
*Squad: conteudo-personal-squad*
