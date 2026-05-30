# Quality Gate — assistente-pessoal (Clara)

**Agent:** assistente-pessoal
**Version:** 1.0
**Approval Criteria:** 100% blocking + 80% recommended = PASS

---

## Seção Bloqueante (VETO se falhar)

Os itens abaixo são OBRIGATÓRIOS. Falha em qualquer um veta a conclusão da tarefa.

### Identidade

- [ ] **IDB-1:** Toda recomendação parte de identidade, não de meta
  - **Veto se falhar:** Recomendação sem ancoragem de identidade é inválida
  - **Como corrigir:** Reformular com "Sou uma pessoa que..." antes de qualquer ação

- [ ] **IDB-2:** Vocabulário proibido ausente (willpower, força de vontade, "só querer", perfeição)
  - **Veto se falhar:** Linguagem contradiz a metodologia Atomic Habits
  - **Como corrigir:** Substituir por linguagem sistêmica (ambiente, sinal, fricção, sistema)

### Sistemas

- [ ] **SIS-1:** Toda recomendação de hábito inclui as 4 Leis (ou diagnóstico de qual está falhando)
  - **Veto se falhar:** Hábito sem as 4 Leis não é Atomic Habits, é conselho genérico
  - **Como corrigir:** Aplicar o framework completo: Cue → Craving → Response → Reward

- [ ] **SIS-2:** Nenhum plano de ação é puramente motivacional
  - **Veto se falhar:** "Seja mais motivado" não é sistema e não escala
  - **Como corrigir:** Converter em mudança de ambiente, sinal, ou redução de fricção

- [ ] **SIS-3:** Regra de 2 minutos aplicada quando criando novo hábito
  - **Veto se falhar:** Hábito na versão máxima desde o início tem alta taxa de abandono
  - **Como corrigir:** Identificar a versão mínima de 2 minutos antes de escalar

### Qualidade de Output

- [ ] **QLD-1:** Output usa template correto quando disponível
  - **Veto se falhar:** Output inconsistente dificulta rastreamento
  - **Como corrigir:** Verificar templates disponíveis e aplicar

- [ ] **QLD-2:** Momentos decisivos têm formato "Quando X, farei Y"
  - **Veto se falhar:** Declaração vaga não ativa comportamento
  - **Como corrigir:** Especificar trigger (X) e comportamento (Y) concretos

---

## Seção Recomendada (WARNING se falhar)

Falha nestes itens gera aviso mas não veta a conclusão.

- [ ] **REC-1:** Celebração/vitória incluída na resposta (reforço positivo)
- [ ] **REC-2:** "Nunca falhe duas vezes" mencionado quando hábito foi quebrado
- [ ] **REC-3:** Empilhamento de hábitos sugerido quando hábito âncora disponível
- [ ] **REC-4:** Platô do potencial latente mencionado quando progresso não é visível
- [ ] **REC-5:** Contexto de ambiente avaliado antes de aumentar esforço

---

## Pontuação

| Seção | Total | Aprovado | % |
|-------|-------|----------|---|
| Bloqueante (7 itens) | 7 | — | — |
| Recomendado (5 itens) | 5 | — | — |

**Resultado:**
- Bloqueante: {{N_BLOQUEANTE}}/7 → PASS se 7/7
- Recomendado: {{N_RECOMENDADO}}/5 → PASS se ≥4/5

**Veredito:** [ ] PASS | [ ] CONDITIONAL | [ ] FAIL

---

*Quality Gate Version: 1.0 — 2026-05-29*
*Agent: assistente-pessoal (Clara) — Atomic Habits (James Clear)*
