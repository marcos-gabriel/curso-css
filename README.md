# Curso CSS
 Curso básico de **CSS** (**C**ascading **S**tyle **S**heet)

 Com o CSS vamos poder customizar nossas páginas HTML e deixar os nossos sites muito mais bonitos!
 CSS descreve como os elementos HTML devem ser exibidos na tela, papel ou em outra mídia. 
 CSS economiza muito trabalho. Ele pode controlar o layout de várias páginas da Web de uma só vez.

 ## Sumário
 1. [Formas de trabalhar com CSS](https://github.com/marcos-gabriel/curso-css#existem-3-formas-de-trabalhar-com-o-css)
    1. [Inline Style](#inline-style)
    1. [Internal Style Sheet](#internal-style-sheet)
    1. [External Style Sheet](#external-style-sheet)
 1. [Seletores](#seletores)
    1. [Seletores simples](#seletores-simples)
        1. [Tags](#tags)
        1. [ID](#id)
        1. [Class](#class)

## Existem 3 formas de trabalhar com o CSS
* External Style Sheet
* Internal Style Sheet 
* Inline Style

### Inline Style
A forma mais simples de se trabalhar com o CSS é implementando a propriedade ` style ` diretamente dentro de nossas tags HTML. Essa propriedade vai ser responsável por aplicar várias formatações de estilo CSS na sua tag correspondente. Obs: Essa é a forma de maior prioridade no CSS, posteriormente você irá entender melhor isso.

Exemplo:
``` html 
<p style="font-family: Arial, Helvetica, sans-serif; background: blue;"> Lorem ipsum dolor sit amet </p> 
```

### Internal Style Sheet
Essa é a forma secundária, e que será a que tem nível intermediário de prioridade da aplicação do estilo CSS. Nessa forma aplicamos todos as formatações CSS dentro da tag ` <style></style> ` que ficará dentro da tag ` <head> ` no nosso arquivo HTML. É nesse momento que vamos começar a ver os chamados **Seletores**, que você entenderá melhor mais na frente.

Exemplo:
``` html
<head>
    <style type="text/css">
        
        p{
            font-family: Arial, Helvetica, sans-serif; 
            background: blue;
        }

    </style>
</head> 

<body>

    <p>Lorem ipsum dolor sit amet</p>

</body>
```

### External Style Sheet
E por último, mas não menos importante, temos o *External Style Sheet*. Pelo nome já dá para perceber que será um arquivo externo, ou seja, agora iremos trabalhar com um arquivo `.css`. Nas duas formas anteriores nós estávamos trabalhando com o CSS dentro do prórpio arquivo HTML, mas agora iremos criar um **novo arquivo** com a extensão `.css` para que ele armazene nossos estilos CSS de maneira mais organizada. Nesse caso você precisará uma tag `<link>` para que possa chamar o arquivo externo CSS. Essa forma é que tem menos prioridade, mas é a mais adequada para trabalhar com o CSS, pois permite uma melhor organização do seu trabalho. 

Exemplo:
* No arquivo HTML:
``` html
<head>
    
    <link rel="stylesheet" type="text/css" href="css/estilo.css">

</head> 

<body>

    <p>Lorem ipsum dolor sit amet</p>

</body>
```
Obs: perceba que a tag `<link>` necessita de algumas propriedades. A propriedade `href` é o caminho para o seu arquivo css, nesse caso foi colocado dentro de uma pasta chamada 'css', e o arquivo é o 'estilo.css'.

* No arquivo CSS:
``` css
p{
    font-family: Arial, Helvetica, sans-serif; 
    background: blue;
}
```

## Seletores
Seletores são elementos que nos ajudam a aplicar formatações CSS para vários componentes HTML ao mesmo tempo. Eles são responsáveis por "encontrar" (ou selecionar) os elementos HTML que você deseja estilizar.
* Seletores simples (tags, id, class)
* Seletores combinados
* Seletores de estado (estado específico de determinados elementos)

### Seletores simples
#### Tags
Tags são os elementos HTML que usamos para estruturar nossas páginas web.

Sintaxe:
``` css
tag-html{
    propriedade-css: valor-da-propriedade;
}
```
Exemplo:
``` css
div{
    width: 600px;
}
```
Nesse exemplo, todas as tags `<div>` irão receber a *width* (largura) de 600px. E, de maneira parecida, poderíamos fazer formatações para todas as outras tags HTML disponíveis no nosso arquivo `.html`.  

#### ID
Os id's são identificadores únicos, que não se repetem. Você pode atribuir id's para elementos HTML usando a propriedade `id` e depois disso você pode formatar o elemento que possui esse id único usando o seletor de id.

Exemplo:

No HTML:
``` html
<body>

    <div id="container">
        <p>Lorem ipsum sit dolor amet</p>
    </div>

</body>
```
No CSS:
``` css
#container{
    width: 700px;
    background-color: red;
}
```
Perceba que para usar o seletor de ID precisamos usar o símbolo de `#` e depois escrever o nome do ID do elemento. Como o ID é um elemento único, não é possível atribuir um ID igual para outros elementos.

#### Class
Já a *Class* (classe), diferentemente do ID, pode ser usada por vários elementos HTML. Você pode atribuir class para elementos HTML usando a propriedade `class` e depois disso você pode formatar os elementos que possuem essa class usando o seletor de class.

Exemplo:

No HTML:
``` html
<body>

    <div id="container">
        <p class="postagem">Lorem ipsum sit dolor amet</p>
        <p class="postagem">Lorem ipsum sit dolor amet</p>
        <p class="postagem">Lorem ipsum sit dolor amet</p>
    </div>

    <div id="container2">
        <p class="postagem">Lorem ipsum sit dolor amet</p>
        <p class="postagem">Lorem ipsum sit dolor amet</p>
        <p class="postagem">Lorem ipsum sit dolor amet</p>
    </div>

</body>
```
No CSS:
``` css
#container{
    width: 700px;
    background-color: red;
}

#container2{
    width: 500px;
    background-color: blue;
}

.postagem{
    font-family: Arial, Helvetica, sans-serif;
    font-size: 16px;
}
```
Nesse caso, perceba que agora nós estamos usando 2 id's, pois não seria possível repetir o mesmo id. Já a `class postagem` foi usada em vários parágrafos simultaneamente e todos eles vão receber a mesma formatação. O seleter de class é o `.` seguido pelo nome da class.
