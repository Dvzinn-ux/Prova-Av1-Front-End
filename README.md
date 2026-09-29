# Prova-Av1-Front-End
# Natação e Suas Utilidades

Este é um projeto de desenvolvimento web focado exclusivamente na estruturação de conteúdo utilizando as especificações do **HTML5**. O site aborda a prática da natação, seus benefícios à saúde, estilos de nado e diretrizes de segurança.

## Diretriz de Desenvolvimento: Sem CSS
Seguindo estritamente os requisitos, o projeto foi desenvolvido **sem nenhuma linha de código CSS**. 
* Não foram utilizadas tags `<style>` ou atributos inline `style=""`.
* Não foram utilizados atributos visuais obsoletos como `align`, `center` ou `cellpadding`.
* Toda a apresentação visual e o comportamento do site dependem exclusivamente da estilização padrão e nativa fornecida pelo navegador.

---

## 📁 Organização de Pastas e Arquivos

A raiz do repositório está organizada da seguinte forma:
```text
├── html/
│   ├── index.html            # Página Inicial (Citações, Contexto, Áudio)
│   ├── beneficios.html       # Benefícios da prática (Tabela 3x3, Medidores)
│   ├── modalidades.html      # Estilos de Nado (Details/Summary, Vídeo)
│   ├── seguranca.html        # Mitos e Dicas (Details/Summary, Correções, Figure)
│   └── contato.html          # Ficha de Pré-Matrícula (Formulário Avançado)
├── img/
│   ├── piscina.jpg           # Imagem utilizada na página index.html
│   └── equipamentos.jpg      # Imagem utilizada na página seguranca.html
├── audio/
│   └── mergulho.mp3          # Arquivo de áudio local tocado no Início
├── video/
│   └── técnica.mp4           # Arquivo de vídeo local rodado em Modalidades
└── README.md                 # Documentação do projeto (Este arquivo)
```

---

##  Recursos Técnicos Implementados

### 1. Estrutura Semântica Completa
Todas as páginas utilizam uma árvore de marcação moderna e estruturada através das tags:
* `<header>` e `<nav>` para cabeçalhos e listas de navegação fluida presentes em 100% das páginas.
* `<main>` para isolar o núcleo de conteúdo de cada tela.
* `<section>` e `<article>` para a correta distribuição temática dos textos.
* `<aside>` para notas de rodapé periféricas e curiosidades rápidas.
* `<footer>` para o encerramento das páginas com dados de autoria e marcação temporal.

### 2. Elementos Gráficos e de Mídia Local (`<figure>` / Mídias)
* **Agrupamento Semântico:** Tags `<figure>` e `<figcaption>` mapeadas com legendas textuais em `index.html` e `seguranca.html`.
* **Mídias Locais:** Inclusão nativa de `<audio src="../audio/mergulho.mp3" controls>` e `<video src="../video/técnica.mp4" controls>` apontando para arquivos reais internos do diretório do projeto.

### 3. Tabela com Dados Reais
Na página `beneficios.html`, foi estruturada uma tabela 3x3 sobre gasto calórico contendo a tag de agrupamento `<thead>` e o atributo de mesclagem vertical **`rowspan="2"`** para unificar o tempo de treino em linhas adjacentes.

### 4. Formulário Avançado
Localizado em `contato.html`, o formulário de matrícula utiliza seletores modernos de validação cliente nativa do HTML:
* Atributos `required` e `placeholder` para experiência e acessibilidade.
* Campos especializados `type="date"`, `type="file"` e `type="range"`.
* Filtro de sugestões utilizando a tag `<datalist>` vinculada dinamicamente ao input de modalidades.

### 5. Marcação Avançada e Elementos Interativos
* **Interatividade Nativa:** Tags `<details>` e `<summary>` empregadas para a construção de sanfonas de conteúdo retrátil nas páginas `modalidades.html` (Estilos) e `seguranca.html` (Perguntas Frequentes).
* **Semântica Textual:** Inclusão precisa das tags `<abbr>` (abreviações com títulos explícitos), `<mark>` (destaques de texto), `<del>` e `<ins>` (indicação de correções textuais históricas), `<blockquote>` e `<cite>` (citações em bloco estruturadas com links externos), além de `<progress>` (barras de progresso) e `<meter>` (indicadores de escala fracionada).
* **Marcação Temporal:** Aplicação da tag `<time datetime="2026-09-29">` mapeando corretamente o dia da realização da avaliação no rodapé.

---

## Autoavaliação e Comentários de Desenvolvimento
Um comentário HTML explicativo (`<!-- -->`) foi adicionado internamente no arquivo `html/contato.html`, detalhando os desafios de escopo e as limitações encontradas ao tentar renderizar valores numéricos dinâmicos para a barra deslizante (`type="range"`) utilizando estritamente marcação pura de hipertexto, sem o apoio de scripts de comportamento ou folhas de estilo.
