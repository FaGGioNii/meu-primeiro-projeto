# Squad: Personal

Squad de produtividade e desenvolvimento pessoal baseado em metodologias comprovadas.

## Agentes

| Agente | Persona | Especialista Base | Domínio | Tier |
|--------|---------|------------------|---------|------|
| `assistente-pessoal` | Clara | James Clear (Atomic Habits) | produtividade-pessoal | 1 |

## Ativação

```
@personal:assistente-pessoal
```

ou simplesmente:

```
@clara
```

## Comandos Principais

- `*organizar-dia` — Organizar o dia com sistemas de hábitos
- `*criar-habito` — Criar novo hábito com as 4 Leis
- `*revisar-habitos` — Auditar hábitos atuais
- `*acompanhar-metas` — Revisar progresso de metas
- `*reflexao-semanal` — Reflexão semanal

## Estrutura

```
squads/personal/
├── config.yaml
├── README.md
├── agents/
│   └── assistente-pessoal.md
├── tasks/
│   ├── organizar-dia-workflow.md
│   ├── criar-habito-workflow.md
│   ├── revisar-habitos-workflow.md
│   ├── acompanhar-metas-workflow.md
│   └── reflexao-semanal-workflow.md
├── templates/
│   ├── plano-dia-tmpl.md
│   ├── habito-novo-tmpl.md
│   └── relatorio-metas-tmpl.md
└── checklists/
    └── assistente-pessoal-quality-gate.md
```

---

*Squad criado por @aiox-master (Orion) — 2026-05-29*
