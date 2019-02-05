# Javascript - Null & Undefined

> Null é **ausência de valor**

> Uma variável é **null** (*nula*) quando ela não é declarada e por consequência, não inicializada

> Uma variável é **undefined** (*indefinida*) quando ela é declarada, mas não inicializada (sem atribuição de valor)



Ao trabalhar com **objetos** (e por consequência, **arrays**), a atribuição ocorre por **referências**

```javascript
const objeto1 = {texto: "Papapa"}
const objeto2 = objeto1
```

No exemplo acima, ambas as contantes (**a** e **b**) recebem a referência (*endereço*) do objeto em questão

Caso o valor da chave **text** seja alterado por qualquer uma das constantes, ambas as constantes "sentirão" a diferença

```javascript
objeto1.texto = "jajaja"
console.log(objeto2) // {texto: "jajaja"}
```



---

Quando se trabalha com **tipos primitivos**, ao fazer uma **atribuição**, ocorre uma **cópia por valor**, uma cópia real

```javascript
let variável1 = 3
let variável2 = variável1
variável2++
console.log(variável2) // 4
console.log(variável1) // 3
```


