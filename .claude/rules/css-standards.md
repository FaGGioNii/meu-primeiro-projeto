---
paths:
  - "**/*.css"
---

# Padrões CSS — Regras de Desenvolvimento

## Mobile First

Todo CSS deve ser escrito **primeiro para telas pequenas** e expandido com `min-width` para telas maiores. Nunca usar `max-width` para sobrescrever estilos mobile.

```css
/* CORRETO — Mobile First */
.card {
  width: 100%;
  padding: 16px;
  font-size: 14px;
}

@media (min-width: 768px) {
  .card {
    width: 48%;
    font-size: 16px;
  }
}

@media (min-width: 1024px) {
  .card {
    width: 30%;
  }
}

/* INCORRETO — Desktop First */
.card {
  width: 30%;
}

@media (max-width: 768px) {
  .card {
    width: 100%;
  }
}
```

**Breakpoints padrão:**

| Nome | Tamanho | Uso |
|------|---------|-----|
| Mobile | base (sem media query) | Padrão — telas até ~767px |
| Tablet | `min-width: 768px` | Tablets e telas médias |
| Desktop | `min-width: 1024px` | Desktops e laptops |
| Wide | `min-width: 1280px` | Telas grandes (opcional) |

---

## Variáveis CSS (Custom Properties)

Toda cor, tamanho de fonte e espaçamento recorrente deve ser definido como variável CSS no `:root`. Nunca repetir valores hardcoded no código.

```css
/* Definição no topo do arquivo CSS */
:root {
  /* Cores */
  --cor-primaria: #1a1a2e;
  --cor-secundaria: #e94560;
  --cor-fundo: #f5f5f5;
  --cor-texto: #333333;
  --cor-texto-claro: #666666;
  --cor-branco: #ffffff;

  /* Tipografia */
  --fonte-principal: 'Inter', sans-serif;
  --tamanho-pequeno: 14px;
  --tamanho-base: 16px;
  --tamanho-medio: 18px;
  --tamanho-grande: 24px;
  --tamanho-titulo: 32px;

  /* Espaçamentos */
  --espaco-pequeno: 8px;
  --espaco-medio: 16px;
  --espaco-grande: 24px;
  --espaco-extra: 48px;

  /* Bordas */
  --borda-raio: 8px;
  --borda-raio-grande: 16px;

  /* Sombras */
  --sombra-card: 0 2px 8px rgba(0, 0, 0, 0.1);
}

/* Uso das variáveis */
.botao {
  background-color: var(--cor-primaria);
  color: var(--cor-branco);
  padding: var(--espaco-pequeno) var(--espaco-medio);
  border-radius: var(--borda-raio);
  font-size: var(--tamanho-base);
}
```

---

## Organização do Arquivo CSS

Seguir sempre esta ordem de seções:

```css
/* 1. Variáveis */
:root { ... }

/* 2. Reset / Base */
*, *::before, *::after { box-sizing: border-box; }
body { margin: 0; font-family: var(--fonte-principal); }

/* 3. Tipografia */
h1, h2, h3 { ... }
p { ... }

/* 4. Layout (header, nav, main, footer) */
header { ... }
nav { ... }
main { ... }
footer { ... }

/* 5. Componentes (botões, cards, formulários) */
.botao { ... }
.card { ... }

/* 6. Utilitários (classes helper) */
.texto-centro { text-align: center; }
.hidden { display: none; }

/* 7. Media Queries (no final) */
@media (min-width: 768px) { ... }
@media (min-width: 1024px) { ... }
```

---

## Regras Gerais

- Usar `box-sizing: border-box` globalmente
- Usar `rem` para fontes, `px` para bordas e sombras, `%` ou `fr` para layouts
- Nomear classes em português com hífen: `.botao-primario`, `.card-aluno`
- Nunca usar `!important` (indica problema de estrutura)
