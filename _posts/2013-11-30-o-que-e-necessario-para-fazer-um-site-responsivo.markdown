---
layout: post
title: O que é necessário para fazer um site responsivo
keywords: "responsive web design, responsive, development, graceful degradation, progressive enhancement"
description: Atualmente com o crescimento do acesso a internet através de dispositivos móveis, se tornou necessário arrumar maneiras de trazer os sites para os smartphones. A partir deste ponto nascem os sites responsivos e/ou adaptivos.
date: 2013-11-30
categories: blog
---

Atualmente com o crescimento do acesso a internet através de dispositivos móveis, se tornou necessário arrumar maneiras
de trazer os sites para os smartphones. A partir deste ponto nascem os sites responsivos e/ou adaptivos.

# Progressive Enhancement
A cada mudança de dispositivo (breakpoint) o  progressive enhancement adiciona funcionalidades para o site de acordo 
com a capacidade de hardware do gadget. Um exemplo é: em um site mobile você não poderá usufruir de todos os efeitos 
em jQuery, já em um tablet essas funcionalidades poderão ser utilizadas com bastante cautela e no desktop sem 
problema nenhum. Tecnicamente o seu projeto fica mais limpo e funcional com a garantia de que tudo irá se ajustar e 
funcionar em todos os dispositivos.

# Graceful Degradation 
É quando utilizamos todos os efeitos e plugins disponiveis fazendo o projeto funcionar em todos os browsers, recheado de conteudo, imagens, menus, etc... Ao utilizar o graceful degradation estaremos removendo funcionalidades do projeto mas sem a garantia que tudo estará perfeito em seu devido lugar levando as famosas “gambiarras” de programador para que tudo se ajuste.

# Mobile First
Inicialmente o site é todo projetado para small-devices como uma “tripa” gigante ocultando o conteudo irrelevante(Como por exemplo: propagandas e banners no caso de portais/blogs) e com funcionalidades básicas de navegação como: menus drop-down simples sem efeitos, textos pequenos e diretos com fontes grandes e imagens escaláveis. Um grande paradigma do mobile first é o content first se preocupando com a apresentação de todo conteúdo relevante, principalmente conteudo de texto que é carregado mais rápido que imagens.

# Planejamento do Mobile First
Ao planejar um futuro site responsivo, não pense em onde o usuário deve clicar, e sim tocar...Uma boa técnica para planejar esses tipos de sites é navegar entre eles e ver a disposição do seu conteúdo, qualidade dos textos, tipos de menus, quantidade de items e o mais importante a facilidade de navegação.

# Layout
Todo baseado em grids o ponto de partida sempre será uma coluna para small-devices e em seguida ir aumentando a largura para:  duas/três colunas para medium-devices e três/quatro colunas para huge-devices (A quantidade de colunas mostradas são apenas exemplos).

# Mantenha tudo adaptavel
Sempre chegamos em um tamanho de tela que praticamente nada fica ligado a nada, é isso que acontece com Tablets quando as imagens não são adaptivas e os textos não são bem elaborados. Mantenha sempre imagens grandes e altere o tamanho do texto de acordo com cada breakpoint e baseie as medidas para imagens sempre em % e textos em EMs.

# Unidades de medida - EMs, PX e %
Medidas são uma coisa importante!. Os EMs são medidas escaláveis que não perdem sua qualidade e são adaptivas. PXs são medida fixas onde podem perder qualidade dependendo de onde for utilizado e % também é escalável mas não adaptiva.

# Desenvolvimento
O segredo do responsivo está nos breakpoints. Existem muitos frameworks de CSS que já criam as grids responsivas como por exemplo: Zurb Foundation e Twitter Bootstrap.  Ou desenvolver-mos um próprio sistema de grids responsivas as nossas necessidades.

# Responsivo e o SEO
Sabendo utilizar as boas práticas de SEO dentro do seu projeto, o site do seu cliente estará sem bem hankeado. Todas as fundamentações do SEO devem ser feitas logo no inicio com a produção dos textos utilizando as palavras chave mais utilizadas pelo Google e uma boa estrutura organizacional dentro do código seguindo os padrões dos buscadores.