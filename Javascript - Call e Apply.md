# Javascript - Call e Apply

> ***Call*** e ***Apply*** são métodos de **funções**, que podem ser usadas para alterar o contexto em que uma função será  executada



```javascript
let objeto1 = {
    chave1: "Olá",
    chave2: 2,
}

let objeto2 = {
    chave1: "Oioi",
    chave2: 666,
}

function função(){
    console.log(this.chave1)
    console.log(this.chave2)
}

função.apply(objeto1) // Olá 2
função.apply(objeto2) // Oioi 666
função.call(objeto1) // Olá 2
função.call(objeto2) // Oioi 666
```

A diferença entre ambas os métodos, é de que o ***call()*** exige que os parâmetros sejam passados diretamente por ele, já o ***apply()*** exige um **array**

```javascript
função.call(contexto, Parâmetro1, Parâmetro2, ...)
função.apply(contexto, [Parâmetro1, Parâmetro2, ...])
```

