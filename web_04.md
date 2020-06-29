# Web 04

## Seção e Tamanho de fonte "em"
- Blocos de conteúdo ```section```, semântica. Diferente de div, que é somente uma divisão visual
- Para comportamento, usa-se id, para estilo, usa-se classes. Nomes de classes devem ser "genéricas", no sentido de não replicar um comportamento: ```.titulo-centralizado``` -> ```.titulo-principal```
- ```font-size: 2em```, em é o tamanho base da fonte, e nesse caso, ela seria 2x o tamanho da fonte base (que é dada em pixels)
- Margem também pode ser em tamanho ```em```

## Posicionamento Float
- Elemento descola da página, mas o restante da página ainda fica em volta dele (todos os elementos abaixo dele são afetados), ```position: float```
- Usa ```float: left``` para quebrar o efeito de float (direita, esquerda, etc)

## Fontes externas
- Google fonts: fontes abertas e preparadas para web
- Pode escrever o texto e visualizar as diferentes fontes
 - Para importar, usa ```link href="endereço"```, e no css colocar no body ```font-family: nome da fonte```
- Para utilizar mapa com localização no site: procura no maps, e na aba da esquerda vai em "compartilhar/incorporar", isso gera um ```iframe``` para a página
 - Pode criar um section para o mapa e estilizá-la
- Usar vídeo do youtube: compartilhar > incorporar, e ele retorna um iframe que possibilita colocar no site
 - Para estilizar, pode usar uma div

## Pseudo-classes e elementos
- ```:hover, :active, :required, :visited, :first-letter, p:first-line```
- Para lista:
```CSS
.itens {
  line-heght: 1.5
}
.itens: first-child{
  font-weight: bold;
}
/*aplica estilo no quarto elemento*/
.itens: nth-child(4){
  font-size: 12px;
}
/*aplica estilo nos pares*/
.itens: nth-child(2n){
  font-size: 12px;
}
```
- Aplicar efeito antes e depois:
```CSS
.titulo-principal:before{
  content: "["
}
.titulo-principal:after{
  content: "]"
}
```
- Pode usar para listas (bolinhas, só usar content com o caracter), títulos de seções

## Background em degradê
- Para a cor de fundo ficar em 100%, é necessário configurar a largura e margin em cada elemento (e não na main geral)
- ```background: linear-gradient(45deg, orange, blue, red, black)```

## Seletores
- Seleção de filhos diretos:
```CSS
main > p {
  background: red;
}
```
 - Seleciona apenas os ```<p>``` que sejam filhos diretos (logo abaixo) da main, se houver outros elementos dentro da main e com ```<p>``` dentro deles, eles não serão afetados
- Pode usar certos elementos com âncora para pegar o próximo elemento, por exemplo: pegar um parágrafo logo após uma imagem, ou pegar todos os parágrafos que são depois de imagem
```CSS
img + p{
  background: blue;
}
img ~ p{
  background: blue;
}
```
- Selecionar todos os ```<p>``` que não são de determinada classe:
```CSS
.principal p:not(#missao){
  background: yellow;
}
```
- Propriedade de cálculo automático: ```width: calc(40% - 26px)```
- Opacidade: ```opacity: 0.7```
- Em títulos e textos, ```color: rgb(0,0,0,0.3)```
- Sombra do elemento: ```box-shadow: X Y cor```, é possível colocar mais de uma sombra ao mesmo tempo
 - Propriedade ```inset``` faz a sombra surgir do centro do elemento
- Sombra em texto: ```text-shadow```

## Design Responsivo
- DPI: densidade de pixel por polegada
- Usa essa tag meta para poder selecionar o tamanho da tela
```HTML
  <meta name="viewport" content="width=device-width">
```
- Media Query (pesquisa, pergunta ao navegador):
```CSS
@media screen and (max-width: 400px){
  body{
    background: red;
  }
}
```
- Usa ```width: auto``` para o elemento pegar a tela completa e redimensionar
