# Javascript - Estrutura de Controle SWITCH

##### A estrutura do Switch

> Para que, um ***switch*** não execute todos os *case's* ao entrar em um, é necessário coloca *break* em todos os fins de *case's*



```javascript
switch(variável){
    case x:
    	// Código
        break
    case y: 
    	// Código
        break
}
```

Caso valores diferentes resultem na mesma ação a ser executada, é possível digitar a ação apenas uma vez

```javascript
switch(variável){
    case x:
    case y: 
    	// Código
        break
}

switch(variável){
    case x: case y: 
    	// Código
        break
}
```

No caso acima, *case x* executará a mesma sentença de código que o *case y*

