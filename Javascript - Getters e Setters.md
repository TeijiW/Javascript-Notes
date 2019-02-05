# Javascript - Getters e Setters

> São métodos que alteram uma variável que é **privada** dentro de um objeto



Estrutura de um ***Get*** e um ***Set***

```javascript
const objeto = {
    _valor: 1, // Convenção, colocar _ quando for uma variável que será privada
	get valor(){
        return this._valor++
	},
	set valor(valor){[
        this._valor = valor
	]}
}

console.log(objeto.valor) // Leitura pelo "get"
objeto.valor = x // Setando valor pelo "set"
```

Como visto acima, a leitura e determinação da variável ocorre por dois métodos, que são chamados quando a linguagem compreendo que o usuário está tentando usar o *get* ou o *set*

Esses métodos são importantes pois, tanto o *get* quanto o *set* podem ser declarados de tal forma que façam validações antes de alterarem de fato uma variável