# Javascript - Funções Callback

> ***Callback*** = "Chamar de Volta"

> Uma função *Callback* é uma função que é chamada quando ocorre um evento



```javascript
let array = ["Texto1","Texto2","Texto3","Texto4"]
function mostrar(nome, indice){
    console.log(`${índice + 1}. ${nome}`)
}

array.forEach(/*Aqui é passado uma função Callback*/)
array.forEach(mostrar)
```

No exemplo acima, foi passado uma função já declarada como parâmetro, mas é possível declarar uma função na hora do callback

```javascript
array.forEach(function mostrarTexto(texto){
    console.log(texto)
})
```

