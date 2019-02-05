# Javascript - Filter

> ***Filter*** é um método que filtra o array, retornando apenas valores que forem de acordo com a função

```javascript
array = [
  {nome:'Teiji', idade:16},
  {nome:'Aaa', idade:20},
  {nome: '2222', idade:15}
]

deMenor = array.filter(function(objeto){
 return objeto.idade < 18
})

console.log(array) // [ { nome: 'Teiji', idade: 16 }, { nome: 'Aaa', idade: 20 },
{ nome: '2222', idade: 15 } ]
console.log(deMenor) // [ { nome: 'Teiji', idade: 16 }, { nome: '2222', idade: 15 } ]
```

