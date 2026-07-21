# 🧬 X-Men — Seleção de Personagens

Interface interativa desenvolvida durante a **Semana do Zero ao Programador Contratado (SZPC)**, promovida pela escola **Dev em Dobro**. O projeto simula a tela de seleção de um jogo de luta (estilo arcade), permitindo que o usuário navegue pela lista de mutantes e veja as informações, nomes e ilustrações em alta resolução atualizados em tempo real.

---

## 🕹️ Funções Existentes

A aplicação foca em dinâmicas de navegação rápida e estados de hover:

*   **Seleção Dinâmica por Hover (`mouseenter`):** Alteração instantânea das informações do personagem ao passar o ponteiro do mouse sobre os cards da lista.
*   **Apresentação em Destaque:** Exibição da ilustração ampliada, nome e descrição biográfica do mutante ativo na coluna lateral.
*   **Indicador Visual de Destaque:** Aplicação de efeito luminoso (`box-shadow` azul brilhante) no card do personagem atualmente selecionado.
*   **Ajuste Automático para Dispositivos Móveis:** Em telas pequenas (menos de 450px), a página realiza uma rolagem suave automática (`scrollTo`) para o topo para garantir que o usuário veja o destaque do personagem ao tocar na lista.

---

## 💻 Recursos de Código

A estrutura explora conceitos essenciais de manipulação do DOM e atributos do HTML5:

*   **Uso de Atributos `data-*` (DataSet):** As descrições (`data-description`) e os nomes (`data-name`) de cada mutante são armazenados diretamente nas tags `<li>` do HTML, sendo extraídos dinamicamente pelo JavaScript via método `getAttribute()`.
*   **Interatividade Procedural Isolada:** Divisão da lógica de troca de contexto em pequenas funções puras (`alterarImagemPersonagemSelecionado`, `alterarNomePersonagemSelecionado`, `removerSelecaoDoPersonagem`), mantendo o código limpo e de fácil leitura.
*   **Camada de Fundo com Pseudo-elemento:** Aplicação da imagem de fundo com efeito de opacidade (`opacity: 0.2`) utilizando o pseudo-elemento `body::before`, garantindo alto contraste e leitura legível para os textos sem afetar os elementos da tela.
*   **Tipografia Temática Customizada:** Incorporação da fonte futurista *Oxanium* via Google Fonts para reforçar a estética geek/arcade.

---

## 🛠️ Stacks Utilizadas

*   **HTML5:** Estrutura declarativa utilizando listas não ordenadas (`<ul>`), tags semânticas (`<main>`, `<section>`, `<header>`) e atributos customizados de dados.
*   **CSS3 Tradicional:** Estilização com Flexbox, uso de pseudo-elementos (`::before`), gerenciamento de profundidade (`z-index`) e regras de responsividade com `media queries` (invertendo o fluxo do layout no mobile via `flex-direction: column-reverse`).
*   **JavaScript (Vanilla JS):** Escuta de eventos de mouse, manipulação de classes no DOM e leitura assíncrona de atributos de dados.

---

## 🎯 Contexto e Propósito Histórico

Este repositório registra uma etapa no aprendizado de lógica front-end durante a formação inicial. O projeto serviu para consolidar a manipulação prática do DOM sem dependência de bibliotecas externas, explorando eventos do mouse e a extração de dados diretamente do HTML. O código permanece em seu estado original desenvolvidos durante a imersão, servindo como registro do avanço nos fundamentos do desenvolvimento web.