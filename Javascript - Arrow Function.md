#	Javascript - Arrow Function

> ***Arrow Function*** é uma forma **reduzida** de declarar uma função

> O contexto de ***This*** em uma *arrow function* não varia, pois o *this* é baseado no **contexto** em que a função foi escrita

> *Arrow Function* é **sempre** uma função anônima, por isso, deve sempre ser armazenada em uma variável ou constante

> Quando se coloca as { }, é obrigatório o uso do ***return***



A estrutura de uma *Arrow Function*

```javascript
let função = function (a) {
    return a*a
} 

função = (Parâmetro1, Parâmetro2, ...) => {
    return Parâmetro1*Parâmetro1
}
```

Caso a função seja curta e haverá apenas um retorno, é possível colocá-la apenas em uma linha

```javascript
função = Parâmetro1 => Parâmetro1*Parâmetro1
```

No exemplo acima, o retorno é **implícito**

```javascript
let função = function(Parâmetro1*Parâmetro1) {
    return "Olá
}

função = () => "Olá"
```

