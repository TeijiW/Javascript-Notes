# Javascript - Try, Catch e Throw



O **try**, faz com que caso ocorra um erro dentro do bloco do mesmo, o código seja direcionado para um tratamento do erro, ou seja, o **catch**, ele faz a parte de tratar o erro de fato.

O **throw** faz a parte de retornar uma mensagem de erro para o código, caso necessário.

Junto do bloco **try/catch**, há o **finally**, que irá executar um bloco de código no fim do bloco do **try**, independente de ocorrer um erro ou não.

Com o **Try** (Tentar) é possível fazer o **tratamento** de um erro

```javascript
const a = undefined
try{
	a.toUpperCase() // Erro, pois toUpperCase() é uma função apenas para strings
} catch { 
	// Tratamento dos erros
    throw "Mensagem"
}
```

