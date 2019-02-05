# Javascript - Declaração de variável com let

> Variáveis declaradas com **let** tem escopo local do bloco em que foram declaradas



É possível relacionar a declaração com ***let*** do Javascript com a de ***private*** do Java

Ao declarar uma variável com ***let***, a variável tem escopo local, independente do bloco de código onde esteja, sendo ele de uma função ou não 

```javascript
let a = 10
{ 
	let a = 20
	console.log(a) // 20
}
console.log(a) // 10
```

