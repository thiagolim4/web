# Web 02

## Menu

- Colocar img dentro de tags ```<h1>``` deixa mesma com mais destaque
- Criar menu usa lista de links
```HTML
<ul>
  <li>Home<\li>
  <li>Produtos<\li>
  <li>Contato<\li>
<\ul>
```
- Tag de âncora, que é um link
```HTML
<a href="index.html">Home<\a>
```  
- Tag ```<nav>``` define links de navegação, geralmente para menus
- Aplicando css, fazendo com que a lista fica um ao lado do outro:
```CSS
nav li {
  display: inline;
}
nav a {
  text-transform: uppercase;
  font-weight: bold;
  text-decoration: none
}
```

## Limpeza de estilo do navegador
- Arquivo ```reset.css``` que zera o estilo que por padrão o navegador utiliza
- Coloca esse arquivo antes da inserção dos outros arquivos css, pois ele limpa tudo antes, se colocar posteriormente ele vai limpar as importações antigas

## Posicionamento
- Posição estática, ponto inicial onde o elemento começa: ```position: static```
- Posição relativa, em relação ao ponto inicial onde ele deveria estar: ```position: relative```
- Posição absoluta, em relação à pagina inteira: ```position: absolute```
 - Caso haja posicionamento absoluto de elementos dentro de outros, o externo (a caixa) deve ter um posicionamento também (relativo, no caso)
- Cálculo automático das laterais da margem: ```margin: 0 auto```
- Em geral, pode usar o margin: auto para blocos, inline-block como display, e o restante vai posicionando
- O navegador soma os pixels de posicionamento + a porcentagem
 - Se por exemplo, usar padding junto com width (%), ele irá somar os pixels do padding com a porcentagem. Para que isso não ocorra, usa-se ```boder-sizing: border-box```, assim o width fica por definitivo, e o padding está dentro desses %

## Bordas
- Cor, largura e estilo separados
```CSS
.produtos {
 border-color: #000000;
 border-width: 2px;
 border-style: solid;
 border-radius: 10px
}
```
- Cor, largura e estilo em uma única propriedade
```CSS
.produtos {
 border: 2px solid #000000;
 border-radius: 10px
}
```

## Semântica
- Conteúdo principal dentro de body, logo abaixo do header: ```<main></main>```
- Área do rodapé fica dentro de ```<footer></footer>```

## Pseudo-classe de estado
- Ações do usuário que podemos mapear para o estilo
- Comportamento de Mouse por cima:
```CSS
nav a:hover{
 color: #FF0000;
 text-decoration: underline  
}
```
- Comportamentos de clique:
```CSS
.produtos li:hover{
  border-color: #00FF00  
}
.produtos li:active{
  border-color: #0000FF
}
.produtos li:hover h2{
  font-size: 40px
}
```
- Colocar imagem de fundo em um elemento (ele repete a imagem para ocupar o elemento completo): ```background: url("bg.jpg");```
- Símbolo do Copyright é um caractere unicode, no site tem as instruções de como utilizar: ```unicode-table.com```. Nesse é ```&copy;``` = &copy;
