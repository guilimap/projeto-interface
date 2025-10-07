# Projeto de Interface: Reconstrução HTML & CSS

Este projeto consiste na reconstrução de interfaces a partir de imagens estáticas, utilizando HTML semântico e CSS moderno. O objetivo é criar páginas responsivas, acessíveis e fiéis ao design proposto, seguindo as diretrizes de organização e boas práticas.

## Telas Implementadas

O CSS está estruturado para suportar diversas telas da aplicação. As páginas que possuem um arquivo HTML correspondente são:

* **`home.html`**: A página inicial da aplicação.
* **`perfil.html`**: A página de gerenciamento de perfil do usuário.

O arquivo de estilos também inclui classes para outras seções, como listagem de posts, formulários de login/cadastro e painéis administrativos, que podem ser implementadas futuramente.

## Decisões de Layout

Para a construção do layout, foram utilizadas tecnologias modernas de CSS, conforme solicitado nos requisitos.

* **Estrutura Principal com Flexbox**: O layout geral da página, incluindo o alinhamento do cabeçalho, rodapé e posicionamento de componentes, foi majoritariamente construído com Flexbox. Isso garante alinhamento e distribuição de espaço de forma eficiente.
* **Grids para Conteúdo**: Para seções que exigem uma organização em múltiplas colunas, como a galeria de categorias populares e o layout da página de perfil, foi utilizado o CSS Grid. Essa abordagem simplifica a criação de layouts complexos e responsivos.
* **Abordagem Mobile-First**: O desenvolvimento seguiu a metodologia *mobile-first*. Os estilos base foram definidos para as menores resoluções, e `media queries` com `min-width` foram usadas para adaptar o layout a telas maiores.
* **Uso de Variáveis CSS**: Para garantir consistência e facilitar a manutenção, todo o projeto utiliza variáveis CSS no `:root` para definir a paleta de cores, as escalas de espaçamento e os tamanhos de fonte.

## Breakpoints Utilizados

O projeto utiliza 3 breakpoints principais para garantir a responsividade em uma vasta gama de dispositivos, desde celulares até desktops.

1.  **Base (Mobile)**: Estilos aplicados a telas com menos de `768px`. O layout é de coluna única e otimizado para toque.
2.  **`@media (min-width: 768px)`** (Tablets):
    * O menu de navegação principal torna-se visível.
    * Layouts como a seção "hero" e cartões de posts passam a ter múltiplas colunas.
    * A grade de categorias populares é ajustada para 3 colunas.
3.  **`@media (min-width: 992px)`** (Desktops Pequenos):
    * O layout da página de perfil é dividido em 2 colunas para melhor aproveitamento do espaço.
4.  **`@media (min-width: 1024px)`** (Desktops Largos):
    * Ajustes finos são aplicados em áreas de conteúdo denso e no espaçamento do cabeçalho.

## Observações de Acessibilidade

Diversas práticas foram adotadas para garantir que a aplicação seja acessível.

* **HTML Semântico**: A estrutura das páginas utiliza tags semânticas como `<header>`, `<main>`, `<footer>`, `<nav>` e `<section>` para dar significado e contexto ao conteúdo.
* **Hierarquia de Títulos**: Os títulos seguem uma ordem lógica (`<h1>`, `<h2>`, etc.), o que facilita a naveção por leitores de tela.
* **Contraste de Cores**: A paleta de cores definida nas variáveis foi escolhida para atender aos critérios de contraste mínimo (AA) da WCAG.
* **Foco Visível em Formulários**: Os campos de formulário (`input`, `textarea`) possuem um indicador de foco claro (`box-shadow`) para auxiliar na navegação via teclado.
* **Ponto de Melhoria**: Foi identificado que o CSS remove o `outline` padrão de links e botões. Embora os formulários tenham um tratamento específico, recomenda-se a implementação de um estado de `:focus-visible` global para todos os elementos interativos, garantindo a conformidade com as boas práticas de acessibilidade.
* **Imagens e Formulários**: A estrutura HTML está preparada para o uso de atributos `alt` em imagens não decorativas e tags `<label>` associadas aos campos de formulário.