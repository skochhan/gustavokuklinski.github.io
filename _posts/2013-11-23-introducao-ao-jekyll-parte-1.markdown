---
layout: post
title: Introducao ao Jekyll - Parte 1
description: Jekyll é uma plataforma para o desenvolvimento de blogs estáticos como esse, ao contrário do Wordpress que dispõe de um banco de dados(MySQL) e utiliza uma linguagem de programação dentro do servidor(PHP). Podemos dizer que esta ferramenta é um blog para "hackers, nerds, geeks ou entusiastas" por sua pequena complexibilidade na hora de criar suas publicações.
date: 2013-11-23
categories: blog curso-jekyll
---

# Introdução
Jekyll é uma plataforma para o desenvolvimento de blogs estáticos como esse, ao contrário do Wordpress que dispõe de um banco de dados(MySQL) e utiliza uma linguagem de programação dentro do servidor(PHP). Podemos dizer que esta ferramenta é um blog para "hackers, nerds, geeks ou entusiastas" por sua pequena complexibilidade na hora de criar suas publicações.
<br />
Foi completamente desenvolvido em Ruby, mas não há necessidade de utilizar um servidor exclusivo para rodar seu blog já que ele "recompila" todo nosso projeto para arquivos estáticos HTML.

# Instalação
Sua instalação é bem simples, porém requer algum conhecimento na linha de comando. Você já deve ter Ruby instalado em sua máquina.
Para instalar basta utilizar o seguinte comando:
{% highlight ruby %}
$ gem install jekyll
{% endhighlight %}
<br />
O Jekyll já vem com um Web servidor embutido, o WebBrick, após realizar a instalação necessitamos iniciar um novo projeto:
{% highlight ruby %}
$ jekyll new meublog
$ cd meublog/
{% endhighlight %}
<br />
Quando um novo projeto é iniciado por padrão ele tem uma estrutura básica:
<br />
<table>
  <tr>
    <td><strong>index.html</strong></td>
    <td>Arquivo que contém o loop de todas as postagens realizadas no blog.</td>
  </tr>
  <tr>
    <td><strong>&#95;config.yml</strong></td>
    <td>Configurações como paginação, nome do blog, etc...</td>
  </tr>
  <tr>
    <td><strong>css/</strong></td>
    <td>Arquivos estáticos em CSS</td>
  </tr>
  <tr>
    <td><strong>&#95;layouts/</strong></td>
    <td>Templates da estrutura básica do HTML e de uma única postagem</td>
  </tr>
  <tr>
    <td><strong>&#95;posts/</strong></td>
    <td>Arquivos MARKDOWN para postagem</td>
  </tr>
  <tr>
    <td><strong>&#95;site/</strong></td>
    <td>Resultado do projeto em HTML com todos os apontamentos certos</td>
  </tr>
</table>

De inicio a pasta <strong>&#95;site/</strong> só é criada quando mandamos o Jekyll compilar o blog.
<br /><br />
# Criando postagens
Para iniciarmos postagens em nosso blog, temos algumas convenções básicas do Jekyll, como por exemplo a nomeclatura do arquivo de postagem.<br />
A nomeclatura segue o seguinte padrão: <strong>ANO-MÊS-DIA-nome-da-postagem.markdown</strong> e deve  ser obrigatóriamente colocado dentro da pasta <strong>&#95;posts/</strong>.<br />
Particularmente gosto de utilizar MARKDOWN, porém há outros tipos de templates disponiveis. Dentro do MARKDOWN temos um cabeçalho que deve ser colocado no topo do nosso arquivo, por convenção já está bem auto explicativo:
{% highlight yaml %}
---
layout: post
title: Titulo da postagem
date: 2013-11-23
categories: categoria sub-categoria
---
{% endhighlight %}
<br />
Na primeira linha: <strong>layout:</strong> é chamado o arquivo: <strong>post</strong> que está na pasta <strong>&#95;layouts/</strong>, então você pode criar vários layouts diferentes para diferentes tipos de postagens.

# Compilando o Blog
Com as postagens realizadas, agora devemos fazer o Jekyll transformar tudo em arquivos estáticos para colocarmos no nosso servidor. Execute o seguinte comando no terminal:
{% highlight ruby %}
$ jekyll serve --watch
{% endhighlight %}
<br />
O paramêtro <strong>serve</strong> inicia o servidor em <strong>http://localhost:4000/</strong> e o <strong>--watch</strong> verifica o projeto procurando mudanças para compila-las automaticamente na pasta <strong>&#95;site/</strong>. Abra o navegador e veja se o blog está funcionando.

# Publicando o Blog em qualquer servidor
O Jekyll é uma solução simples para quem deseja ter um blog estático e simplório.<br />
Para realizar o deploy do seu blog no servidor basta copiar os arquivos de dentro da pasta <strong>&#95;site/</strong> para o servidor via FTP.

# Considerações finais
Dúvidas, deixem comentários...Espero que tenha ajudado com esta breve introdução sobre Jekyll...Este é o primeiro de uma série de "aulas" sobre Jekyll que estou desenvolvendo :)