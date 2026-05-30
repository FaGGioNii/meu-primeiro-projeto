# Task: Criar Post

**Task ID:** criar-post
**Version:** 1.0
**Purpose:** Criar conteúdo completo para Instagram ou WhatsApp na voz do Hendrew Faggioni
**Agent:** redator-conteudo (Leo)
**Mode:** Interactive

---

## Inputs

| Parâmetro | Tipo | Obrigatório | Descrição |
|-----------|------|-------------|-----------|
| `tema` | string | Sim | Tema do conteúdo (pode vir do briefing do @pesquisador-tendencias) |
| `formato` | string | Sim | "reels", "carrossel", "foto", "story", "whatsapp-broadcast", "whatsapp-individual" |
| `angulo` | string | Não | Ângulo específico (se não informado, definir no Step 1) |
| `cta_objetivo` | string | Não | "lead", "engajamento", "salvar", "compartilhar" (padrão: lead) |

---

## Contexto Fixo — Não Modificar

**Quem é o Hendrew:**
- Personal trainer, Franca-SP
- Studio semi-privado (presencial, capacidade máxima atingida)
- Consultoria online: R$ 99,90/mês — plano trimestral
- Tom: direto, sem rodeios, baseado em resultado real
- NÃO usa: linguagem corporativa, promessas vazias, "lifestyle"
- USA: exemplos concretos, dores reais, resultados tangíveis

**Público-alvo da consultoria online:**
- Adultos com rotina ocupada que treinam ou querem treinar em casa
- Já tentaram fazer sozinhos — algum nível de ceticismo com promessas
- Buscam acompanhamento real, não planilha genérica
- Não são especialistas em fitness — linguagem deve ser acessível

---

## Steps

### Step 1: Definir Ângulo e Gancho

**Ação:**
- Se ângulo não foi informado, definir com base no tema:
  - Qual dor específica do público este tema endereça?
  - Qual percepção errada o público tem sobre este tema?
  - Qual resultado tangível está conectado a este tema?
- Criar 2-3 opções de gancho para o formato escolhido
- Selecionar o gancho mais direto e que melhor nomeia a dor/desejo

**Critérios do gancho:**
- Para nos primeiros 2 segundos de scroll
- Nomeia uma dor real ou faz uma promessa específica
- Não começa com "Você sabia que..." — muito genérico
- Evitar clickbait — o conteúdo deve entregar o que o gancho promete

**Output:** `angulo_definido` + `gancho_escolhido`

---

### Step 2: Escrever o Corpo do Conteúdo

**Ação por formato:**

**Reels (legenda):**
- Gancho (1-2 linhas)
- [espaço em branco]
- Contexto ou promessa em 2-4 linhas
- [espaço em branco]
- CTA direto
- [espaço em branco]
- Hashtags (bloco separado)

**Carrossel (slides):**
- Slide 0 (Capa): Promessa ou pergunta — máx 6-8 palavras visíveis
- Slides 1-N: Um ponto por slide — título curto + 1-3 linhas de explicação
- Slide final: CTA + convite a salvar
- Legenda: Gancho + 2-3 linhas + CTA + hashtags

**Foto:**
- Legenda: Gancho + conteúdo em 3-6 linhas + CTA + hashtags
- Usar quebras de linha para facilitar leitura
- Máx 150-200 palavras no corpo

**Story:**
- Máx 3 linhas por tela
- Tom de conversa direta
- Se tiver enquete: pergunta curta com opções claras

**WhatsApp broadcast:**
- Abertura: "Oi! " ou "Olá, pessoal!"
- Uma ideia central por mensagem
- Tom pessoal, como mensagem de um amigo que é personal
- CTA suave no final
- Máx 150 palavras

**WhatsApp individual:**
- Contexto da conversa no topo (para guiar o Hendrew)
- Mensagem completa pronta para copiar/colar
- Tom ainda mais pessoal — usa nome se disponível

**Output:** `rascunho_completo` — conteúdo no formato solicitado

**Veto conditions:**
- Linguagem que soaria estranha se o Hendrew falasse em voz alta → REESCREVER
- Promessa sem base (ex: "emagreça 5kg em 1 semana") → SUBSTITUIR por resultado realista
- Jargão técnico sem explicação (ex: "hipertrofia sarcoplasmática") → SIMPLIFICAR

---

### Step 3: Definir Hashtags (Instagram apenas)

**Ação:**
- Selecionar 8-15 hashtags em 3 camadas:
  - **Alta concorrência (2-3):** #personaltrainer #treino #fitness
  - **Média concorrência (4-6):** #treinoencasa #consultoriaonline #treinofuncional #emagrecer
  - **Nicho/local (2-4):** #francasp #personaltraineronline #treinopersonalizado #resultado

**Output:** `hashtags_selecionadas` — bloco de hashtags

---

### Step 4: Revisar Voz e Tom

**Ação:**
- Ler o rascunho em voz alta (simular a experiência do Hendrew lendo)
- Verificar:
  - Soa como o Hendrew ou como uma empresa?
  - Alguma linha soa "marketeirês" ou artificial?
  - O CTA é de baixo atrito (pede pouco) ou de alto atrito (pede muito)?
- Aplicar ajustes necessários

**Output:** `rascunho_revisado` — versão final antes de enviar para @revisor-publico

---

## Veto Conditions

| Condição | Ação | Razão |
|----------|------|-------|
| Gancho genérico ("Você sabia que...") | REESCREVER gancho | Não para o scroll |
| CTA ausente | ADICIONAR CTA antes de entregar | Conteúdo sem CTA não converte |
| Linguagem corporativa | SUBSTITUIR por linguagem do Hendrew | Quebra autenticidade |
| Promessa exagerada | AJUSTAR para resultado realista | Gera desconfiança no público cético |

---

## Output Format

### Para Instagram (Reels/Foto):
```
**LEGENDA — [Formato] — [Tema]**

---
[Gancho]

[Corpo do conteúdo]

[CTA]
---

**Hashtags:**
[bloco de hashtags]
```

### Para Carrossel:
```
**CARROSSEL — [Tema]**

**Slide 0 (Capa):** [texto da capa]
**Slide 1:** [título] — [texto]
**Slide 2:** [título] — [texto]
...
**Slide Final:** [CTA + salvar]

**Legenda:**
---
[Gancho + corpo resumido + CTA + hashtags]
---
```

### Para WhatsApp:
```
**MENSAGEM — WhatsApp [Broadcast/Individual] — [Objetivo]**

---
[Mensagem completa]
---

*Nota para o Hendrew: [instrução opcional de uso]*
```

---

## Completion Criteria

- [ ] Gancho definido e testado contra os critérios
- [ ] Corpo no formato correto para o canal escolhido
- [ ] CTA claro e presente
- [ ] Hashtags selecionadas em 3 camadas (se Instagram)
- [ ] Tom do Hendrew verificado na leitura em voz alta
- [ ] Rascunho pronto para @revisor-publico

---

*Task Version: 1.0 — 2026-05-30*
