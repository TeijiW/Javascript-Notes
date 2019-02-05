# Javascript - Arrays

> Os arrays em Javascript são **heterogêneos**, ou seja, permitem diversos tipos de dados, porém, a **boa prática** diz que se deve criar apenas arrays **homogêneos** 

> Os arrays em Javascript não tem **tamanho fixo**, como ocorre no Java ou na Golang

> Os arrays em Javascript são **objetos**

```
Um array é simbolizado por [ ]
```



#### Declaração de Arrays

```javascript
let array = [/*Elementos*/]
let array = new Array(/*Elementos*/)
```





**array.length** - Retorna a quantidade de elementos de um array

```javascript
let array = [1,2,3]
console.log(array.length) // 3
```

**array.push(Elementos)** ou **array[índice] = elemento **- Adiciona um ou mais elementos no fim do array

```javascript
let array = ['a','b']
array.push('c')
console.log(array) // ['a','b','c']
```

**array.unshift()** - Adiciona um ou mais elementos no ínicio do array

```javascript
let array = ['a','b']
array.unshift('c')
console.log(array) // ['a','b','c']
```

**array.pop()** - Deleta/Retira o último elemento do array

```javascript
let array = ['a','b','c']
array.pop()
console.log(array) // ['a','b']
```

**array.shift(índice)** - Deleta/Retira o primeiro elemento do array

```javascript
let array = ['a','b','c']
array.shift()
console.log(array) // ['b','c']
```

**delete array.[índice]** - Deleta o elemento do índice indicado

```javascript
let array = ['a','b','c']
delete array.[1]
console.log(array) // ['a',<1 empty item>,'c']
```

**array.splice(índice do ínicio, índice de vezes, elementos para adicionar)** - Deleta, adiciona ou substitui um elemento do array

```javascript
let array = ['a','b','c']
array.splice(1, 2, 'x','y')
console.log(array) // ['a','x','y']
```

**array.concat(arrays)** - Concatena arrays

```javascript
let array = ['a','b','c']
newArray = array.concat(['d','e','f'])
console.log(newArray)
```

