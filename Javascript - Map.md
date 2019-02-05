# Javascript - Map

> ***Map*** é um método que retorna um novo array **do mesmo tamanho** com alterações 

Ele recebe como parâmetro uma função ***callback***, essa ***callback*** recebe três parâmetros, o elemento, o índice do mesmo e o próprio array. É possível ignorar ambos os parâmetros.

```javascript
const array = [1,2,3,4,5]
const array1 = array.map(function(elemento){
  return elemento*2
})
console.log(array1) // [2,4,6,8,10]
```

