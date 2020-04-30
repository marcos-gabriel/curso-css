# Curso CSS
 Curso básico de CSS (Cascading Style Sheet)

 Com o CSS vamos poder customizar nossas páginas HTML e deixar os nossos sites muito mais bonitos!

 ## Sumário
 1. [Existem 3 formas de trabalhar com o CSS](https://github.com/marcos-gabriel/curso-css#existem-3-formas-de-trabalhar-com-o-css)
    1. [Inline Style](#inline-style)
    1. [Internal Style Sheet]()
    1. [External Style Sheet]()
 1. [Seletores]()

## Existem 3 formas de trabalhar com o CSS
* External Style Sheet
* Internal Style Sheet 
* Inline Style

### Inline Style
A forma mais simples de se trabalhar com o CSS é implementando a propriedade ` style ` diretamente dentro de nossas tags HTML. Essa propriedade vai ser responsável por aplicar várias formatações de estilo CSS na sua tag correspondente. Obs: Essa é a forma de maior prioridade no CSS, posteriormente você irá entender melhor isso.
Exemplo:
``` html 
<p style="font-family: arial, helvetica, sans-serif; background: blue;"> Lorem ipsum dolor sit amet </p> 
```

### Internal Style Sheet
Essa é a forma secundária, e que será a que tem nível intermediário de prioridade da aplicação do estilo CSS. Nessa forma aplicamos todos as formatações CSS dentro da tag ` <style></style> ` que ficará dentro da tag ` <head> ` no nosso arquivo HTML. É nesse momento que vamos começar a ver os chamados **Seletores**, que você entenderá melhor mais na frente.
Exemplo:
``` html
<head>
    <style type="text/css">
        
        p{
            font-family: arial, helvetica, sans-serif; 
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
    font-family: arial, helvetica, sans-serif; 
    background: blue;
}
```

## Seletores
