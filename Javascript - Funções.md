# Javascript - Funções

> Uma função é basicamente, uma **ação**, ela uma executa **ação** baseada em uma **sentença de código**

> Uma função é um **bloco de código**

> **Parâmetros** são opcionais

> **Retorno** é opcional



A função em JS é First-Class Object (Citizens). Ou seja, High-order function



#### Declarando uma função

Uma função pode ser declarada de diversas maneiras, uma delas é a **literal**

```javascript
function nomeDaFunção(Parâmetro1, Parâmetro2, ...){
    //Código
}
```

Outra forma é declarando funções **anônimas**, que é basicamente armazernar uma função em uma **variável** ou **constante**

```javascript
const nomeDaFunção = function (Parâmetro1, Parâmetro2, ...){
    //Código				
}
```

Por ser justamente um dado, é possível **armazernar** funções em arrays.

```javascript
const array = [function(Parâmetro1, Parâmetro2){ return Parâmetro1+Parâmetro2 }]
```

O mesmo serve para **objetos**

```javascript
const objeto = {}
objeto.falar = function(Parâmetro1, Parâmetro2, ...){ return "Olá" }
```

Além do modo tradicional, atualmente há também uma maneira reduzida, chamada de **arrow function**

```javascript
const nomeDaFunção = (Parâmetro1, Parâmetro2, ...) => {
    //Código				
}
```



#### Passando Parâmetros

> Caso um parâmetro **não** seja recebido, ele será definido como *undefined* **caso** ele não tenha um valor padrão

É possível passar funções como parâmetros também

```javascript
function nomeDaFunção(Função){
    Função()
}
```



##### Parâmetros Variáveis

É possível fazer com que a função espere parâmetros de forma variável, com **array *arguments***, que está presente em toda função, carregando dentro dele todos os parâmetros passados.

```javascript
function nomeDaFunção (){
	let soma = 0
    for (i in arguments){
        soma += arguments[i]
    }
}
```



##### Parâmetro com Valor Padrão

É possível fazer com que caso os parâmetros necessários **não sejam passados**, assumam um  determinado valor

```javascript
function(Parâmetro1, Parâmetro2, ...){
    Parâmetro1 = Parâmetro1 || 1
    Parâmetro2 = Parâmetro2 || 1
}
```

Apesar de muito utilizada, a estratégia acima não é válida se por acaso, o parâmetro (caso recebido) for 0, pois 0 assumiria *false*.

Há outras três maneiras, utilizando o operador ternário

```javascript
function(Parâmetro1, Parâmetro2, ....){
    Parâmetro1 = Parâmetro1 ==! undefined? a : 1
    Parâmetro2 = 1 in arguments? Parãmetro2 : 1 // O 1 varia conforme a posição do argumento
    Parâmetro3 = isNaN()? 1 : Parâmetro3
}
```

Com o ES2015, há uma forma oficial de fazer essa padronização dos valores dos argumentos

```javascript
function (Parâmetro1 = x, Parâmetro2 = y, ...){
    // Código
}
```

