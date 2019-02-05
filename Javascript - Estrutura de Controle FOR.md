# Javascript - Estrutura de Controle FOR
##### A estrutura do FOR
```javascript
for(/*contador;condição/incrementador*/){
  // Código
}
// Exemplo
for(let i=1;i <= 20;i++){
  // Código
}
```
É possível também, percorrer um **array** com o FOR
```javascript
for(let i=1;i<array.length;i++){
  console.log(array[i])
}
```

Há uma forma cuja qual retorna o **índice** de cada elemento do array

```javascript
for(let i in array){
    console.log(i) // Retornará os índices
}
```

É possível utilizar a estrutura **FOR/IN** para **objetos** também

```javascript
for(let i in objeto){
    console.log(i) // Retornará as chaves
}
```

