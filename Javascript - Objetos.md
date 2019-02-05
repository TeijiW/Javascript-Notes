# Javascript - Objetos

> O objeto em Javascript é basicamente uma coleção de **chaves** e **valores**

>Os objetos em Javascript são **dinâmicos**

> Tentar acessar algo que está dentro de um atributo *undefined* causa erro



```javascript
Um objeto é simbolizado por { } normalmente
```

Há duas maneiras de se criar um **objeto**

```javascript
const objeto = { }
const objeto = new Object
```

Além das formas mostradas acima, ainda é possível criar um objeto com uma **função construtora** ou com uma **Função Factory**

É possível criar atributos para um objeto de forma **dinâmica**

```javascript
const objeto = { }
objeto.chave = valor // Com notação ponto
objeto["chave"] = valor // Com acesso por colchetes
```

Ou seja, mesmo depois de declarado e inicializado, um objeto pode receber **novas chaves**

Uma forma de criar **objetos** com mais facilidade, é colocar apenas o nome da variável/constante, assim, a **chave** será o nome da variável e o **valor** será o valor da variável/constante

```javascript
const nome = "Teiji"
const idade = 16

const pessoa = { nome, idade }
console.log(pessoa) // { nome: "Teiji", idade: 16 }
```

É  possível **deletar** chaves de um objeto

```javascript
delete objeto.chave1 
delete objeto["chave1]	
```



Uma constante armazena a referência para o **endereço de memória** para o objeto. e quando se altera as chaves e valores de um objeto, a referência não é mudada

A função chamada ***freeze*** literalmente congela um objeto, não possibilitando alteração, adição ou exclusão das chaves e valores

```javascript
Object.freeze(objeto)
objeto.chave10 = 231313 // A Atribuição não ocorre
```



---

#### Outras funções



.keys( ) - Retorna um array com as chaves do objeto

.values( ) - Retorna um array com os valores do objeto

.entries( ) - Retorna um array com as chaves e os valores do objeto

.defineProperty( ) - Define as propriedades de uma chave/valor

.assign( ) - Concatenação de Objetos



```javascript
objeto = {
    chave1: "Valor1",
    chave2: "Valor2",
    chave3: "Valor3",
}

console.log(Object.keys(objeto)) // ['chave1','chave2','chave3']
console.log(Object.values(objeto)) // ['valor1','valor2','valor3']
Object.defineProperty(objeto, 'chave4', {
    enumerable: true,
    writable: false,
    value: '01/01/2019',
})
```

É possível também "**concatenar**" objetos

```javascript
objeto1 = {
    chave1: "A"
}
objeto2 = {
    chave2: "B"
}
objetoReceptor = {
    chave3: "C"
}
objetoFinal = Object.assign(objetoReceptor, objeto1, objeto2)
console.log(objetoFinal)
```

Caso tenha alguma chave **idêntica** em algum dos objetos, apenas o último objeto passado como parâmetro será levado em conta