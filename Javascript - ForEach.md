# Javascript - ForEach

>  ***ForEach*** é uma função para array que percorre o array

Ele recebe como parâmetro uma função ***callback***, essa ***callback*** recebe três parâmetros, o elemento, o índice do mesmo e o próprio array. É possível ignorar ambos os parâmetros.

```javascript
let array =  ['John','Holden','Bill']
array.forEach(function(nome, indice){
    console.log(`${indice} - ${nome}`)
})
```

