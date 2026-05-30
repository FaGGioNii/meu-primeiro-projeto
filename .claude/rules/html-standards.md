---
paths:
  - "**/*.html"
---

# Padrões HTML — Regras de Desenvolvimento

## Estrutura Obrigatória

Todo arquivo HTML deve começar com esta estrutura base:

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Título da Página</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>

</body>
</html>
```

**Regras inegociáveis:**
- `lang="pt-BR"` sempre presente na tag `<html>`
- `charset="UTF-8"` sempre presente
- `viewport` meta tag sempre presente (base para mobile-first)
- `<!DOCTYPE html>` sempre na primeira linha

---

## HTML Semântico

Usar sempre elementos semânticos — nunca `<div>` onde existe um elemento com significado.

| Em vez de | Use |
|-----------|-----|
| `<div class="header">` | `<header>` |
| `<div class="nav">` | `<nav>` |
| `<div class="main">` | `<main>` |
| `<div class="section">` | `<section>` |
| `<div class="article">` | `<article>` |
| `<div class="aside">` | `<aside>` |
| `<div class="footer">` | `<footer>` |
| `<div class="button">` | `<button>` |

**Estrutura semântica padrão de página:**

```html
<body>
  <header>
    <nav>...</nav>
  </header>

  <main>
    <section>...</section>
    <section>...</section>
  </main>

  <footer>...</footer>
</body>
```

---

## Acessibilidade Básica

- Toda `<img>` deve ter atributo `alt` descritivo
- Todo `<input>` deve ter `<label>` associado
- Botões devem ter texto descritivo (não apenas ícone)
- Usar `<button>` para ações, `<a>` para navegação

```html
<!-- Correto -->
<img src="treino.jpg" alt="Aluno fazendo agachamento no studio">
<label for="nome">Nome completo</label>
<input type="text" id="nome" name="nome">

<!-- Incorreto -->
<img src="treino.jpg">
<input type="text" placeholder="Nome">
```

---

## Organização de Arquivos

- Um arquivo CSS externo por página (não usar `<style>` inline)
- Scripts JS no final do `<body>`, antes de `</body>`
- Nunca usar `style=""` diretamente nas tags HTML

```html
<!-- Correto -->
<body>
  <!-- conteúdo -->
  <script src="script.js"></script>
</body>

<!-- Incorreto -->
<p style="color: red;">Texto</p>
```
