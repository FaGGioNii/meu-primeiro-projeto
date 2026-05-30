# conteudo-personal-squad

Squad para criação de conteúdo de Instagram e WhatsApp para a consultoria online do **Faggioni Personal Studio**.

**Versão:** 1.0.0
**Autor:** Hendrew Faggioni
**Criado em:** 2026-05-30

---

## O que este squad faz

Orquestra 3 agentes especializados para produzir conteúdo pronto para publicar:

1. **Iris** (@pesquisador-tendencias) — Pesquisa o que está em alta no nicho fitness
2. **Leo** (@redator-conteudo) — Escreve posts e mensagens na voz do Hendrew
3. **Maya** (@revisor-publico) — Revisa e garante que o conteúdo ressoa com o público

---

## Como usar

### Fluxo completo (recomendado)

```
1. Ativar Iris:   /AIOX:agents:pesquisador-tendencias
2. Iris pesquisa: *pesquisar-tendencias  OU  *briefing-semanal

3. Ativar Leo:    /AIOX:agents:redator-conteudo
4. Leo escreve:   *criar-post [tema]  OU  *criar-mensagem [objetivo]

5. Ativar Maya:   /AIOX:agents:revisor-publico
6. Maya revisa:   *revisar
7. Maya aprova:   *aprovar  →  Conteúdo pronto! ✅
```

### Fluxo rápido (quando já tem o tema)

```
1. Leo escreve:  *criar-post [tema específico]
2. Maya revisa:  *revisar
3. Publicar
```

---

## Agentes

| Agente | Persona | Quando usar |
|--------|---------|-------------|
| `pesquisador-tendencias` | Iris (Analyst) | Início do processo — descobrir o que postar |
| `redator-conteudo` | Leo (Creator) | Escrever posts Instagram e mensagens WhatsApp |
| `revisor-publico` | Maya (Guardian) | Revisar e aprovar antes de publicar |

---

## Formatos suportados

| Formato | Agente | Comando |
|---------|--------|---------|
| Instagram Reels | Leo | `*criar-post [tema]` + formato=reels |
| Instagram Carrossel | Leo | `*criar-carrossel [tema]` |
| Instagram Foto | Leo | `*criar-post [tema]` + formato=foto |
| Instagram Story | Leo | `*criar-post [tema]` + formato=story |
| WhatsApp Broadcast | Leo | `*criar-mensagem [objetivo]` |
| WhatsApp Individual | Leo | `*criar-mensagem` + formato=individual |
| Sequência de posts | Leo | `*criar-sequencia [tema]` |

---

## Estrutura do Squad

```
squads/conteudo-personal-squad/
├── squad.yaml                          # Manifest
├── README.md                           # Este arquivo
├── agents/
│   ├── pesquisador-tendencias.md       # Iris — pesquisadora
│   ├── redator-conteudo.md             # Leo — redator
│   └── revisor-publico.md              # Maya — revisora
├── tasks/
│   ├── pesquisar-tendencias-task.md    # Workflow de pesquisa
│   ├── criar-post-task.md              # Workflow de criação
│   └── revisar-post-task.md           # Workflow de revisão
├── workflows/
│   └── pipeline-conteudo-semanal.md   # Pipeline completo dos 3 agentes
├── templates/
│   ├── post-instagram-tmpl.md         # Template Instagram
│   └── mensagem-whatsapp-tmpl.md      # Template WhatsApp
└── checklists/
    └── quality-gate-conteudo.md       # Checklist de aprovação
```

---

## Público-alvo do conteúdo

O conteúdo deste squad é criado para:
- Adultos com rotina ocupada que treinam ou querem treinar em casa
- Pessoas com algum ceticismo (já tentaram e não tiveram resultado)
- Público que busca acompanhamento real, não planilha genérica
- Nível de conhecimento fitness: básico a intermediário

---

## Produto que o conteúdo promove

- **Consultoria online de personal trainer**
- **Preço:** R$ 99,90/mês no plano trimestral
- **Diferencial:** Treino personalizado para a realidade do aluno, não planilha genérica

---

*Squad Version: 1.0.0 — 2026-05-30*
