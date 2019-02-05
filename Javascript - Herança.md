# Javascript - Herança

É possível saber qual é o objeto **pai** de um objeto

```javascript
console.log(objeto.__proto__) // Objeto Pai 
```

Um objeto criado por padrão referencia ao bojeto pai ***Object.prototype***

O ***Object.prototype*** não tem pai



---

#### Cadeia de protótipos (prototype chain)

```javascript
const objeto1 = { 
	chave1: 'A'
}
const objeto2 = { 
	__proto__: objeto1, 
	chave2: 'B'
}
const objeto3 = { 
	__proto__: objeto2, 
	chave3: 'C'
}
```

Um atributo pode sobreescrever outro caso esteja **acima** na **cadeia de protótipos**

Caso o **atributo procurado** no escopo "atual" não seja encontrado, o atributo é procurado nos escopos maiores

Há outra forma de relacionar um prototype

```javascript
const objeto1 = {
    funcao1(){
        // Código
    }
}
const objeto2 = {
    chave1: "A",
    funcao2(){
        return super.funcao1
    }
}

Object.setPrototypeOf(objeto1, objeto2) // (Filho, Pai)
```

E outra

```javascript
const pai = {
    // Código
}

const filho = Object.create(pai) 
```

É possível ainda, editar o Objeto Deus (Pai de todos), colocando um atributo global

```javascript
Object.prototype.atributo1 = "A"
```

O mesmo ocorre caso seja criada uma função construtora

```javascript
function objetoPersonalizado (){}
objetoPersonalizado,prototypeatributo1 = "B"
```

Para checar se um atributo é da classe/objeto herdada, ou um atributo próprio, se utiliza o ***.hasOwnProperty***

**Exemplo**

```javascript
const carro = {
  modelo: "",
  velAtual: 0,
  velMax: 0,
  acelerar(vel){
    if ((this.velAtual + vel) <= this.velMax){
      this.velAtual += vel
    }else{
      this.velAtual = this.velMax
    }
  },
  mostrar(){
    return `${this.velAtual}KM/H de ${this.velMax}KM/H`
  }
}

const gol = {
  modelo: "Gol 2015",
  velMax: 150,
  mostrar(){
    return `${this.modelo}: ${super.mostrar()}`
  }
}

const toro = {
  modelo: "Toro Freedom 2019",
  velMax: 300,
}

Object.setPrototypeOf(gol,carro)
Object.setPrototypeOf(toro,gol)

toro.acelerar(300)
gol.acelerar(50)

console.log(gol.mostrar())
console.log(toro.mostrar())
```

