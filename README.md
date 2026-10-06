# 📱 TechNews Today - Portal de Tecnologia

Página web de um portal de notícias de tecnologia, criada como desafio de **HTML5 + CSS3**. O projeto usa tags semânticas, um layout moderno com **Grid**, efeito **glassmorphism** no cabeçalho e um design responsivo com tema escuro.

## 📂 Estrutura do projeto

```
📁 projeto/
├── 📄 index.html        # Estrutura da página (HTML)
└── 🎨 10a_desafio.css   # Estilização da página (CSS)
```

> O HTML está vinculado ao CSS pela tag `<link rel="stylesheet" href="10a_desafio.css">`.

## 🧱 Estrutura do HTML

A página é organizada com tags semânticas:

| Elemento | Classe | Descrição |
|---|---|---|
| `<header>` | `.cabecalho` | Logo "TechNews Today" e tagline com `<strong>` e `<em>` |
| `<main>` | `.conteudo` | Área principal da página (layout em grid) |
| `<article>` | `.artigo-destaque` | Notícia em destaque: título, data (`<time>`) e texto |
| `<details>` | `.leia-mais` | Bloco expansível "Leia mais" com `<summary>` |
| `<section>` | `.secao-video` | Vídeo do YouTube incorporado via `<iframe>` |
| `<section>` | `.secao-newsletter` | Formulário de inscrição na newsletter |
| `<footer>` | `.rodape` | Direitos autorais e contato por e-mail (`<address>`) |

### 📝 Formulário da newsletter

- **E-mail** (`type="email"`, obrigatório)
- **Área de interesse** (`<select>`): Inteligência Artificial, Desenvolvimento Mobile ou Tecnologias Web
- **Aceite dos termos** (`type="checkbox"`, obrigatório)
- **Botão** "Inscrever-se" (envio por `POST` para `subscribe.php`)

## 🎨 Estilização (CSS)

### Paleta de cores

| Uso | Cor |
|---|---|
| Fundo da página | `#0a0e27` |
| Texto principal | `#e4e4e7` |
| Tagline | `#94a3b8` |
| Títulos / links | `#60a5fa` |
| Data / rodapé | `#64748b` |
| Destaque "Leia mais" | `#f59e0b` |
| Gradiente do logo | `#6366f1` → `#db2777` |
| Gradiente do card | `#1e293b` → `#334155` |
| Gradiente da newsletter | `#6366f1` → `#8b5cf6` |
| Gradiente do botão | `#f59e0b` → `#ef4444` |

### Principais técnicas utilizadas

- **Reset global** (`margin`, `padding` e `box-sizing: border-box`)
- **Glassmorphism** no cabeçalho: gradiente translúcido + `backdrop-filter: blur(10px)`
- **Cabeçalho fixo** com `position: sticky`, `top: 0` e `z-index: 100`
- **Texto com gradiente** no logo usando `background-clip: text`
- **CSS Grid** no `.conteudo` (`display: grid`, `gap: 30px`, largura máxima de `800px`, centralizado)
- **Cards modernos** com bordas arredondadas (`border-radius: 20px`) e borda translúcida
- **Efeitos de hover**:
  - Artigo sobe levemente: `transform: translateY(-5px)`
  - Botão aumenta: `transform: scale(1.05)`
- **Transições suaves** com `transition`
- **Campos do formulário** com fundo translúcido e bordas arredondadas
- **Vídeo** com borda colorida (`2px solid #6366f1`) e cantos arredondados

### 📱 Responsividade

Em telas com largura mínima de **768px** (`@media (min-width: 768px)`):

- O grid passa a ter duas colunas (`2fr 1fr`)
- O artigo em destaque ocupa as duas colunas (`grid-column: span 2`)

A abordagem é **mobile-first**: o layout padrão é de uma coluna e se expande em telas maiores.

## 🚀 Como executar

1. Salve os dois arquivos na mesma pasta (o HTML e o `10a_desafio.css`).
2. Abra o arquivo HTML em qualquer navegador moderno (Chrome, Firefox, Edge, etc.).

> ⚠️ O envio do formulário depende de um arquivo `subscribe.php` e de um servidor com PHP (como XAMPP). Sem isso, o botão de inscrição não terá efeito.

## 🛠️ Tecnologias

- HTML5
- CSS3 (Grid, Gradientes, Backdrop Filter, Media Queries)

## 📌 Observações

- O ícone/emoji dos títulos e o vídeo do YouTube exigem conexão com a internet.
- Projeto desenvolvido para fins de estudo.

---

© 2025 TechNews Today • Todos os direitos reservados