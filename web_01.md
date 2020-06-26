# Web 01

## Tags de HTML:
- ```<h1>``` para níveis de cabeçalho
- ```<p>``` parágrafo
- ```<en>``` itálico
- ```<strong>``` negrito
- ```<!DOCTYPE html>``` não precisa ser fechada, no topo da página, informa a versão do HTML sendo usada (nesse caso é a última disponível)
- ```<html lang="pt-br">``` tag de conteúdo da página, oferece a opção de tradução caso não seja a língua nativa do visitante
- ```<meta charset="UTF-8">``` passa informações pro navegador da codificação dos caracteres, no caso esse dicionário (UTF-8) contém a maioria dos caracteres utilizados
- ```<title>``` nome da aba
- Estrutura do navegador:
 - ```<html lang="pt-br">``` engloba toda a página
 - ```<head>``` informações que ta passando pro navegador (meta, e title)
 - ```<body>``` toda info que quer exibir (todo o restante)

## CSS (folha de estilo em cascata):
- Tudo que se adiciona no elemento pai reflete para o filho
- Em ```<p>```:
 - ```style = font-size: 16px; text-alig: center; background: #CCCCCC```, forma inline
- Para aplicar em várias tags entre ```<style>```:
```CSS
body {
  background: #CCCCCC
}
p {
 text-align: center
}
em strong {
  color: red
}
```
- Importar o arquivo css:
```<link rel = "stylesheet" href="style.css">```
- Representação de cores em hexadecimal:
```CSS
# RR GG BB
# _ _ _ _ _ _
```
 - Preto = 00 00 00
 - Branco = FF FF FF
 - Red = FF 00 00
 - Green = 00 FF 00
 - Blue = 00 00 FF
- Fomato RGB:
 - rgb(255,255,255)
- Nomes:
 - red, green, blue

## Marcadores e Imagens
- Acrescentando identificador (id) no HTML:
```HTML
<p id="missao">
```
- No CSS:
```CSS
#missao {
  font-size: 20px
}
```
- Inserir imagem:
```HTML
<img src="caminho da img">
```
 - height: 100px (altura absoluta)
 - width: 50% (largura em relação ao tamanho da tela)
 - border: finalização do elemento (externo)
 - padding: espaçamento interno (se aumentar, em geral aumenta o tamanho do elemento)
 - margin: espaçamento externo da borda

## Listas, DIVs e Header
- ```<ul>``` Lista não ordenada
 - ```<li>``` List item
- ```<ol>``` Lista ordenada
- Classes no css, diferente do id, são repetíveis
 - ```<li class="itens">```
 - Colocando classe no css:
 ```CSS
 .itens {
   font style: italic
 }
 ```
- Criar blocos de conteúdo: ```<div>```
- Comportamento display block e inline:
 - **Block:** ocupa a largura inteira da página
 - **Inline:** permite inserir outros elementos em sua lateral
 - **Inline-block:** ele bloqueia a largura, mas ela é fixa, dada por mim
 ```CSS
 ul {
   display: inline-block;
   vertical-align: top
 }
 ```
 - Alinhamento vertical (vertical-align), por padrão o inline-block alinha pela base do item (imagem)
- ```<header>``` tag semântica, cabeçalho da página, dentro do conteúdo (body). Define o conteúdo principal da página, em geral com ```<h1>```
