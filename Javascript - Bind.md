# Javascript - Bind

> O ***Bind*** é responsável por determinar em que contexto será executado o método chamado

```javascript
const objeto = {
    texto: "Olá Mundo",
    mostrarTexto(){
        console.log(this.texto)
    }
}

objeto.mostrarTexto() // Olá Mundo
const variável1 = objeto.mostrarTexto 
console.log(variável) // undefined
const variável2 = objeto.mostrarTexto.bind(objeto) 
console.log(variável2) // Olá Mundo
```

O *Bind* não altera a função cujo qual ele atua, ele cria uma nova.