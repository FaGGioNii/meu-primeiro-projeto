# Convenções Git — Regras do Projeto

## Conventional Commits em Português

Todo commit deve seguir o formato:

```
<tipo>: <descrição curta em português>
```

**Tipos permitidos:**

| Tipo | Quando usar | Exemplo |
|------|-------------|---------|
| `feat` | Nova funcionalidade | `feat: adiciona página de contato` |
| `fix` | Correção de bug | `fix: corrige alinhamento do menu mobile` |
| `style` | Mudanças visuais sem alterar lógica | `style: ajusta cores do botão primário` |
| `refactor` | Reorganização de código sem mudar comportamento | `refactor: reorganiza variáveis CSS` |
| `docs` | Documentação | `docs: atualiza README com instruções de uso` |
| `chore` | Tarefas de manutenção | `chore: adiciona arquivo .gitignore` |
| `remove` | Remoção de arquivos ou funcionalidades | `remove: deleta página antiga de preços` |

---

## Regras da Mensagem

**Descrição curta:**
- Sempre em português
- Letra minúscula após o tipo (exceto nomes próprios)
- Sem ponto final
- Máximo 72 caracteres
- Verbo no infinitivo ou presente: "adiciona", "corrige", "atualiza"

```bash
# Correto
git commit -m "feat: adiciona formulário de contato"
git commit -m "fix: corrige espaçamento no mobile"
git commit -m "style: atualiza paleta de cores do studio"

# Incorreto
git commit -m "mudanças"
git commit -m "Feat: Adiciona Formulário De Contato."
git commit -m "update"
git commit -m "wip"
```

---

## Fluxo de Trabalho

```bash
# 1. Verificar estado antes de qualquer operação
git status

# 2. Adicionar arquivos específicos (nunca git add . sem revisar)
git add index.html
git add style.css

# 3. Commit com mensagem descritiva
git commit -m "feat: adiciona estrutura base da landing page"

# 4. Push via @devops (exclusivo)
# Ativar @devops para executar git push
```

---

## O Que Nunca Fazer

- `git add .` sem antes verificar o que será commitado com `git status`
- Commits com mensagem vaga: "atualização", "mudanças", "wip", "teste"
- Commits com múltiplas funcionalidades não relacionadas — um commit por mudança lógica
- Commitar arquivos sensíveis (senhas, tokens, arquivos `.env`)
- `git push --force` na branch `main`

---

## .gitignore Padrão para Este Projeto

Manter sempre no `.gitignore`:

```
# Ambiente
.env
.env.local

# Sistema operacional
.DS_Store
Thumbs.db

# Editor
.vscode/
.idea/

# Dependências (quando usar Node.js futuramente)
node_modules/
```
