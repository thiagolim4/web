# Web 3

## Formulários

- Dentro das tags ```<form></form>```
- Inputs possuem ids (identificadores, únicos)
 - E também utilizam labels, e pode usar label for com o mesmo id do input (criando "pares")
- Botão: input com type="submit"
```CSS
form {
  margin: 40px 0;
}
form input {
  display: block
}
form label, form p {
  display: block;
  font-size: 20px
}
```
- Textarea é uma tag de conteúdo, em que o usuário pode colocar mais de uma linha de texto (define o número de linhas e o número de colunas)
- Radiobox é mais de uma opção, referente ao mesmo input, e para o mesmo grupo usa-se o mesmo "name" (e para posicionar usa ```fieldset```, com ```legend```)
- Checkbox é o "check", pode marcar e desmarcar itens
- Seletor (select) geram listas de itens (dropdown)
- Site Mobile Input Types pode ver como os inputs se comportam nos celulares
- Required indica um campo obrigatório
- Placeholder = texto prévio no campo (mais claro)
- Inputs de celular: ```email, tel, number, password, date, datetime, month e search```

## Hierarquia no CSS
- Inline (1k) > Id (100) > Class (10) > Tag (1)
- Id se sobressai em relação às classes, que sobrepõem as tags
- Se só tem tags, conjuntos de tags são prioritárias

## Transição de efeito
- Propriedade ```transition: 1s bakground```, entre normal e hover
- ```transform: scale(1.2)```, quando passa o mouse no elemento e ele muda seu tamanho (de acordo com o número definido)
- ```transform: rotation(70deg)```, faz rotação
- Para usar ambas, coloca as propriedades juntas, pois se colocar uma abaixo da outra, prevalece a última

## Tabelas
- Existem tags semânticas para a tabela, cabeçalho (thead) e corpo (tbody), e se quiser rodapé (tfoot)
```HTML
<table>
  <thead>
    <tr>
      <th></th>
      </tr>
      </thead>
  <tbody>
    <tr>
      <td></td>
    </tr>
  </tbody>
</table>
```
- Para estilizar/organizar pode usar padding para as tags th e td
- Para mesclar células, usa-se o ```colspan=X```
