---
layout: post
title: Utilizando data-uri
keywords: "técnica, web design responsivo, rwd, data url, data uri, data, url, uri"
description: Data URI é um técnica utilizada para otimizar o carregamento de recursos dentro do servidor web. É ideal para trabalhar em design responsivo pois tenta manter a imagem com o máximo de qualidade independente do tipo de medida utilizada.
date: 2013-11-25
categories: blog tutorial
---

Data URI é um técnica utilizada para otimizar o carregamento de recursos dentro do servidor web. É ideal para 
trabalhar em design responsivo pois tenta manter a imagem com o máximo de qualidade independente do tipo de
medida utilizada.

# O que é Data URI ?
Data URI são imagens em formato de dado bruto codificado em Base64. Dados brutos tem uma simplicidade maior
de serem processados no servidor sem uma nova requisição, mas utilizando a potencia de hardware do servidor
web como: memória e processador.

Trecho de Data Uri:
{% highlight bash %}
S+L6eG7PV5/R8r........R8Y8fHfzfnTv7vb
{% endhighlight %}
<br />

# Como converter JPG,GIF,PNG ?
Existem diversos serviços online para converter imagens como: [Data URI Converter](http://dataurl.net/#dataurlmaker)
ou caso precise de um conversor offline, pode-se utilizar o comando 'base64' presente em todos sistemas Unix.
{% highlight bash %}
$ base64 imagen.png | tr --delete '\n' > output.txt
{% endhighlight %}
<br />

# Utilizando Data-uri
Para utilizar é como criar imagens em HTML ou CSS<br />
HTML:
{% highlight html %}
<img src="data:image/jpeg;base64,S+L6eG7PV5/R8r........R8Y8fHfzfnTv7vb" alt="" />
{% endhighlight %}
<br />
CSS:
{% highlight css %}
background: url("data:image/jpeg;base64,S+L6eG7PV5/R8r........R8Y8fHfzfnTv7vb");
{% endhighlight %}
<br />
Caso tenha criado a data uri através do comando UNIX, o resultado será um dado bruto. Para utiliza-lo
é necessário que adicione o tipo de arquivo antes do código em base64: 'data:image/jpeg;base64,'.

# Vantagens
Rápido carregamento no servidor.<br />
Não há necessidade de caminhos absolutos/relativos dentro da URL.<br />
Grandes imagens sempre estarão leves e com qualidade.<br />

# Desvantagens
Necessidade de sempre criar um novo código caso tenha alteração na imagem.<br />
Caso tenham muitas imagens o arquivo principal pode demorar para carregar.<br />