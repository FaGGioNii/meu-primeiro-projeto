# Dev Agent Memory (Dex)

## Active Patterns
<!-- Current, verified patterns used by this agent -->

### Key Patterns
- CommonJS (`require`/`module.exports`), NOT ES Modules
- ES2022, Node.js 18+, 2-space indent, single quotes
- Absolute imports always (never relative `../`)
- kebab-case for files, PascalCase for components
- Jest 30.2.0 for testing, `npm test` to run

### Project Structure
- `.aiox-core/core/` — Core modules (synapse, session, code-intel, orchestration)
- `.aiox-core/development/` — Agents, tasks, templates, scripts
- `.aiox-core/infrastructure/` — CI/CD, git detection, project-status
- `tests/` — Test suites (mirrors source structure)
- `docs/stories/` — Story files (active development)

### Frontend Web Patterns (Faggioni Personal Studio)
- **HTML**: semântico obrigatório — `<header>`, `<main>`, `<section>`, `<footer>`, nunca `<div>` onde existe elemento com significado
- **HTML**: `<html lang="pt-BR">`, `charset="UTF-8"`, viewport meta — sempre presentes
- **HTML**: toda `<img>` com `alt` descritivo; nunca `style=""` inline; scripts no final do `<body>`
- **CSS**: mobile-first — estilos base sem media query, expandir com `min-width: 768px` e `min-width: 1024px`
- **CSS**: nunca usar `max-width` para sobrescrever mobile — apenas `min-width`
- **CSS**: variáveis no `:root` obrigatórias — nunca valores hardcoded repetidos
- **CSS**: paleta do projeto → `--cor-primaria: #0d0d0d`, `--cor-acento: #25D366`, `--cor-fundo: #f5f5f5`
- **CSS**: nomes de classes em **português com hífen** — `.botao-whatsapp`, `.secao-hero`, `.card-resultado`
- **CSS**: nunca usar `!important`
- **Zero dependências externas** — HTML e CSS nativos, sem frameworks, sem CDN, sem JS

### Git Rules
- NEVER push — delegate to @devops
- Conventional commits **em português**: `feat:`, `fix:`, `style:`, `refactor:`, `docs:`, `chore:`, `remove:`
- Descrição em minúsculo, verbo no infinitivo, sem ponto final, máximo 72 caracteres
- Exemplos corretos: `feat: adiciona seção de depoimentos`, `fix: corrige botão flutuante no iPhone`
- Nunca: `git add .` sem revisar `git status` antes

### Common Gotchas
- Windows paths: use forward slashes in code, bash shell not cmd
- `fs.existsSync` for sync checks, `fs.promises` for async
- atomicWriteSync from `.aiox-core/core/synapse/utils/atomic-write` for safe file writes
- CodeRabbit runs in WSL, not Windows directly

### Story Workflow
- Read task → Implement → Write tests → Validate → Mark checkbox [x]
- ONLY update: checkboxes, Debug Log, Completion Notes, Change Log, File List
- NEVER modify: Status, Story, AC, Dev Notes, Testing sections

## Promotion Candidates
<!-- Patterns seen across 3+ agents — candidates for CLAUDE.md or .claude/rules/ -->
<!-- Format: - **{pattern}** | Source: {agent} | Detected: {YYYY-MM-DD} -->
- **NEVER push — delegate to @devops** | Source: dev, analyst, sm, data-engineer, ux, qa (6 agents) | Detected: 2026-02-22 | Status: Already elevated to `.claude/rules/agent-authority.md`
- **CommonJS module system (require/module.exports)** | Source: dev, analyst, sm, data-engineer, ux, architect (6 agents) | Detected: 2026-02-22 | Status: Already in CLAUDE.md (Padroes de Codigo)
- **Conventional commits format** | Source: dev, devops, analyst, sm, data-engineer, ux (6 agents) | Detected: 2026-02-22 | Status: Already in CLAUDE.md (Convencoes Git)
- **kebab-case for files** | Source: dev, analyst, sm, data-engineer, ux (5 agents) | Detected: 2026-02-22 | Status: Already in CLAUDE.md (Padroes de Codigo)

## Archived
<!-- Patterns no longer relevant — kept for history -->
<!-- Format: - ~~{pattern}~~ | Archived: {YYYY-MM-DD} | Reason: {reason} -->
