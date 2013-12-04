# Lição 1: A internet

## Introdução

Você já se perguntou como a Internet funciona? Claro que sim! Hoje você vai aprender como fazer sites, logo você também vai poder contribuir para construí-la. Sites são escritos em __HTML__, que significa __Linguagem de Marcação Hipertexto__. Você irá entenderá mais sobre isso enquanto constrói sua página.

## Passo 1: O que são sites?

1. Abra um __editor de textos__. (Não pode ser Word, ok?)
2. Crie um novo documento. 
3. Escreva algo, por exemplo:
`Olá! Meu nome é …`
4. Salve o arquivo. Nomeie ele de `ola.txt`.
5. Feche tudo e abra o arquivo novamente. Abril o editor de texto, né? Mas isso não é tão legal.
6. Mude a extensão do arquivo (sobrenome, são as letrinhas que vem logo após o PONTO) para `.html`, então agora o arquivo terá o nome de `hello.html`.
7. Abra o arquivo novamente.

Que programa foi usando para abrir o arquivo dessa vez? O navegador é um programa especial que sabe como intepretar textos escritos utilizando __linguagem HTML__. Nós não adicionamos nenhum __HTML__ ainda, nós simplesmente colocamos o mesmo texto, mas o navegador não se importa muito com isso! Assim que você lhe fornece um arquivo `.html`, ele irá fazer o máximo para exibir o arquivo como ele compreende.

Isso é muito útil: toda vez que um site possui erros, o navegador irá tentar encontrar uma maneira de exibi-lo de alguma forma.

__Como nós podemos ver esses arquivos?__

Quanto você escreve um endereço no seu navegador, sua requisição chega a um computador que está configurado para permitir como exibir páginas de internet que estão armazenadas nele. Esse computador é chamado de servidor. Quando ele recebe uma pedido do seu computador, ele busca todos os arquivos necessários: o arquivo `html` e todo o resto de coisas que a página precisa, como imagens e vídeos.

// diagrama de como a web funciona - deve dizer no cabeçalho: Posso ter essa página por favor? e na base: Lá vamos nós!

## Passo 2: O que é HTML?

HTML é uma linguagem de __marcação__ que signifca que ela será usada para descrever o que as coisas são.

Mesmo que o navegador tente exibir as coisas da melhor forma possível, isso irá lhe ajudar a entender o que são essas coisas.

Para dizer ao navegador que, vamos usar `tags`.

Tags se parecem com isso:
`<p>Alguma coisa escrita.</p>`

`<p>` é a abreviação de __parágrafo__.

Abrimos a tag com isso:
`<p>`
e fechamos uma tag parecido com a anterior, adicionando uma barra:
`</p>`
O navegador entende que tudo que estiver entre duas tags desse tipo é um parágrafo de texto.

Tags podem conter configurações, que podem ser bem úteis.
Vamos dar uma olhada em uma tag de link:
`<a href="http://codeclub.org.uk">Visite o site do CodeClub Brasil</a>`
`<a>` é uma abreviação de __âncora__, que é como os links são chamados.

Ele também possui uma tag de abertura:
`<a>`
e outra para fechar
`</a>`
mas nós também adicionamos uma configuração junto a tag de abertura:
`<a href="http://codeclub.org.uk">`
`href` é a configuração, e `http://codeclub.org.uk` é o valor.
`href` significa _referencia de hipertexto_. Um texto que possui link, pode se conectar com outros textos. Que faz com que ele seja um pouquinho diferente do que um texto normal.
`html` diz para o navegador para onde o link deverá levar, e o texto entre as tags será o que ficará marcado como link.

1. Abra o arquivo `page.html`.
2. Pergunte ao voluntário se você pode usar um Óculos de Raio-X ou as ferramentas de desenvolvedor para ver o código (desenvolvedor é alguém que faz coisas com códigos).


#### If you can use X-Ray Goggles:
3. Click on the X-Ray Goggles bookmarklet. 
4. Move your mouse around the page. You can see the parts of the page light up, and see what tags they are made of. You can click on each box to see the snippet of code the box is made of.

#### If you are using developer tools:
3. Move around the page. Right click anything interesting, and then click `Inspect element`. A panel will open up which will show you the page's code as the same time as the page.
4. Move your mouse over different pieces of code. The corresponding things on the page will be highlighted, so you can see which bit does what.
5. Try to inspect all parts of the page. Can you figure out what the different tag names stand for?

We already know `<p>` and `<a>`.
`<ol>` - ordered list 
`<ul>` - unordered list
`<li>` - list item
`<h1>`, `<h2>`, `<h3>`, `<h4>`, `<h5>`, `<h6>` - headings
`<hr>` - horizontal rule
`<div>` - a box for grouping things
`<img>` - a special element, which unlike others doesn't have a closing tag. We use it for putting the images in.

There are also some tags that we will always use in HTML documents, and they are:
`<html>` - tells the browser where we put out code
`<head>` - inside `<head>` we put things which may be useful to the browser, but which don't appear as text on the page. In this example we put a `<title>` there, which then shows up at the top of the browser window.
`<body>` - that's where we put the things we want to appear on the page

6. Notice how tags can __nest__ within one another. We have the `<a>` tag, which is inside a `<p>` tag, which in turn is inside `<div>`, which is placed inside `<body>`.

Whenever this happens, we say that the tag that is being wrapped is the _child_ and the tag that does the wrapping is the __parent__ element. It's a little bit like a family tree!

7. To the browser all tags of the same kind are the same, but you can mark them out using classes and Ids (pronounced aye-dees). 
For example, some of your paragraphs might be introductions, so you could give them a class `introduction`. See if you can spot some classes inside `page.html` .

8. Ids are used to mark unique items on your page. See if you can spot the `div` tag with an `id` of `kitten` in the page.

9. What will happen if you move things around? Let's go back to the code editor. Find an `<ol>` tag in the code and select it with all its got inside, like so:

```HTML
<ol>
	<li>Kittens</li>
	<li>Cake</li>
	<li>Lie-ins</li>
	<li>Playing games</li>
</ol>
```

Now copy it and move it somewhere else. Save the page and refresh it in the browser. How does the order of your code affect the order in which things are displayed in the browser?

## Things to try

* Create your own paragraph of text.
* Make a link that points to another part of page (hint: it is something to do with id - look out for a link that takes you to the kitten).
* Add your own headings where you think they might be useful. What happens if you change the heading numbers, for example from `<h3>` to `<h4>`?
* What would you have to do to link to a different page?
* If you are using developer tools, once you bring up the panel with the code try double-clicking on the code that looks interesting. See if you can change it. Now you get a live preview without having to move between the browser and the code editor. Cool, huh? Now refresh the page. What happened? When you edit code like this it doesn't get saved, so you can preview what would happen if you did, but don't mess up your file, so you can experiment lots and always go back.





