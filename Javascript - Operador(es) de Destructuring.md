# Javascript - Operador(es) de Destructuring

> Quando utilizado no contexto de um **objeto**, se utiliza **{ }** no Destructuring

> Quando utilizado no contexto de um **array**, se utiliza **[ ]** no Destructuring

 

**Destructuring** (Desestruturação) é uma maneira de **extrair** de um **atributo** de um **objeto** 

```javascript
const pessoa = {
    nome: "Teiji",
    idade: 16,
}

const { nome, idade } = pessoa
console.log(nome, idade) // Teiji 16
```

É possível também, extrair atributos que estão **dentro de outros atributos**

```javascript
const pessoa = {
    nome: "Teiji",
    idade: 16,
    endereço: {
        rua: "F"
        numero: 26
    }
}

const { endereço: { rua, numero } } = pessoa
console.log(rua, numero) // F 26
```

Caso seja tentado extrair um atributo que está dentro de um atributo **inexistente**, será retornado erro. 

Há também uma forma de atribuir os dados a variáveis

```javascript
const pessoa = {
    nome: "Teiji",
    idade: 16,
}

const { nome: n, idade: i } = pessoa
console.log(n, i) // Teiji 16
```



Caso seja tentado extrair um atributo **não existente**, ele retornará como valor *undefined*.

Uma forma de evitar isso é atribuir um **valor padrão**

```javascript
const pessoa = {
    nome: "Teiji",
    idade: 16,
}

const { sobrenome = "Default", legal = False } = pessoa
console.log(sobrenome, legal) // Default False
```



---

##### Destructuring  em Arrays

> Caso seja tentado extrair um valor inexistente, é retornado **undefined**



Para extrair um determinado elemento de um array e atribuí-lo a uma variável, basta colocar o nome da variável entre [ ]

```javascript
const [a] = 10
console.log(a) // 10
```



É possível também, "ignorar" elementos que estão num array

```javascript
const [n1, ,n2, ,n3,n4] = [1,2,3,4,5]
console.log(n1,n2,n3,n4) // 1 3 5 undefined
```



É possível obter o valor de elementos que estão **dentro de um array** que está **dentro de outro array**

```javascript
const [, [, n1]] = [1, [10,9]]
console.log(n1) // 9
```

Porém, é um código de **difícil leitura** e até **ineficiente**



---

##### Destructuring em Funções



Uma outra possibilidade é passar como parâmetro para uma função, um destructuring 

```javascript
function nomeDaFunção({ valor1, valor2 }){
    //Código
}

const objeto = { 
	valor1: x, 
	valor2: y 
}

nomedaFunção(objeto)		
```

Sendo assim, ao passar um objeto como agumento ao chamar a função, o destructuring é feito "automaticamente".

É possível passar um objeto sem nenhuma chave ou sem alguma das chaves, mas, caso **não seja** passado nenhum objeto, ocorre um **erro**, pois aí a linguagem estaria tentando desestruturar algo inexistente.



Assim como com os **objetos**, é possível utilizar de **destructuring em arrays** nas funções

```javascript
function nomeDaFunção([ valor1, valor2 ]){
    //Código
}

nomeDaFunção([x,y])
```

Assim como ocorre com os objetos, caso não seja passado nada (nem um array vazio), ocorre um erro, pois a linguagem tenta desestruturar elementos de um array nulo, inexistente.