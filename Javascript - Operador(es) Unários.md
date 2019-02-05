# Javascript - Operador(es) Unários

> Há duas maneiras de executar os Operadores Unários, de forma **prefixada** e de forma **pósfixada**



Préfixada - A ação do operador unário é executada **antes** da expressão em questão utilizar do número

Pósfixada - A ação do operador unário é executada **depois** da expressão utilizar o número



**++** - Operador de adição (1)

**--** - Ooperador de subtração (1) 



```javascript 
const a = 1 

// Forma Pósfixada
console.log(--a) // 0 
console.log(++a) // 2
// Forma Préfixada
console.log(a--) // 1
console.log(a++) // 1
```

Apesar da facilidade em utilizar esses operadores, **não é recomendado** utilizá-los em comparações, por exemplo