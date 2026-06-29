# 🦅 Império Bizantino

Site educacional sobre o Império Bizantino, desenvolvido como Trabalho N3 da disciplina de **Ferramentas Web e UX**.

---

## 1. Escopo Fechado

### Objetivo
Apresentar de forma interativa e visualmente rica a história, inovações, política e cultura do Império Bizantino — do seu apogeu no século IX até a queda de Constantinopla em 1453.

### Público-alvo
Estudantes e entusiastas de história medieval que buscam um ponto de entrada acessível e bem organizado sobre o tema.

### Por que Bizâncio?
O grupo tem afinidade com história, e o Império Bizantino foi uma escolha natural: é um dos impérios mais subestimados da história, com mais de mil anos de duração, inovações militares e culturais únicas e um legado que moldou o mundo moderno. Um dos integrantes defendeu o tema com entusiasmo e o grupo topou.

### Paleta de Cores

| Variável | Cor | Razão |
|---|---|---|
| `--color-primary` | `#5E1934` — vinho imperial | O roxo/vinho era a cor exclusiva dos imperadores bizantinos (*porphyrogennetos*) |
| `--color-accent` | `#D4AF37` — ouro | Remete ao ouro dos mosaicos e moedas *Solidus* do império |
| `--color-secondary` | `#1F305E` — azul profundo | Evoca o Mar Mediterrâneo e o céu dos mosaicos de fundo dourado |
| `--bg-primary` | `#F4F0EC` — pergaminho | Remete à textura de manuscritos e documentos históricos da época |
| `--color-terracotta` | `#A23A36` — terracota | Usado para ameaças externas na linha do tempo política |

### Tipografia
**Josefin Sans** (Google Fonts) — escolhida por combinar legibilidade moderna com traços geométricos que remetem à elegância clássica, sem cair em fontes serifadas que dificultam a leitura em tela.

### Framework
Nenhum. O projeto foi desenvolvido com **HTML5, CSS3 e JavaScript puro**, o que foi suficiente para atender todos os requisitos sem dependência de ambiente de execução.

---

## 2. Estrutura do Site

### `index.html` — Home
Página principal com três seções:
- **Introdução** com o propósito do site e símbolo imperial
- **O Nascimento de Bizâncio** — card com imagem e texto sobre a origem do império a partir da divisão romana e a Dinastia Macedônica
- **Principais Inovações** — quatro seções alternadas imagem/texto cobrindo: Fogo Grego, Preservação Cultural, Arquitetura Monumental e Alfabeto Cirílico
- **A Queda de Constantinopla** — seção de encerramento com imagem e impacto histórico do fim do império em 1453

### `galeria.html` — Galeria
Grid responsivo com 19 imagens históricas (mosaicos, manuscritos, arquitetura, moedas, mapas). Ao passar o mouse sobre cada imagem, uma legenda descritiva surge com animação de deslize, identificando o que é retratado e o período histórico.

### `politica.html` — Política
Linha do tempo com quatro momentos decisivos da história política bizantina: **1025** (Apogeu de Basílio II), **1118** (Restauração Comnena), **1265** (Restauração de Constantinopla) e **1453** (Queda). Cada era apresenta imagem, resumo e dois blocos destacando ameaças internas e externas daquele período.

### `contato.html` — Área do Cidadão
Formulário de registro com validação em JavaScript:
- **Nome**: mínimo de 3 caracteres
- **E-mail**: validação via Regex (`/^[^\s@]+@[^\s@]+\.[^\s@]+$/`)
- **Senha Imperial**: mínimo de 7 caracteres
- **Mensagem**: campo opcional
- Erros exibidos inline sem uso de `alert()`
- Envio bem-sucedido abre um **modal animado** de confirmação com opção de fechar

### Componentes globais
- **Header fixo** com logo (Águia Bicéfala) e navegação com indicador de página ativa
- **Menu hambúrguer** em mobile (≤700px): links surgem da esquerda para a direita em cascata com animação
- **Footer** em todas as páginas com lista de integrantes e citação de Nicéforo II Focas

---

## 3. Integrantes

| Nome | O que desenvolveu |
|---|---|
| **Brayan Marques Eger** | Página `index.html` — estrutura da home, seções de inovações, nascimento de Bizâncio e queda de Constantinopla |
| **Felipe** | Esqueleto do site — estrutura base HTML, CSS global (`styles.css`), componentes reutilizáveis de header e navegação |
| **Jonathan Felipe Dinis Kovaleski** | Página de imperadores (a ser adicionada) — pesquisa e desenvolvimento da seção dedicada aos imperadores bizantinos |
| **Samuel Lampert Alchini** | Página `politica.html` — linha do tempo política com eras, ameaças internas/externas; integração final do projeto e unificação dos arquivos do grupo |

---

## 4. Decisões Técnicas

- **Mobile First**: media queries aplicadas a partir de `480px`, `700px` e `900px`
- **Acessibilidade**: tags semânticas (`<header>`, `<main>`, `<nav>`, `<section>`, `<article>`, `<footer>`, `<figure>`, `<figcaption>`, `<blockquote>`, `<cite>`), atributos `alt` em todas as imagens e `aria-expanded` no botão hambúrguer
- **Heurísticas de Nielsen**: feedback visual em inputs (`:focus` com borda dourada), mensagens de erro específicas por campo (Heurística 9 — Prevenção de Erros), modal de sucesso com animação (Heurística 1 — Visibilidade do Status)
- **Sem banco de dados**: todas as interações são client-side, conforme especificação
