# Javascript - Operador(es) Relacionais

> Comparações com operadores relacionais sempre retornarão **true** (verdadeiro) ou **false** (falso)



**==** - Comparação de **igualdade** de **valores**

**===** - Comparação de **igualdade** de **valores** e **tipos**

**!=** -  Comparação **negativa** de igualdade de **valores**

**!==** - Comparação **negativa** de igualdade de **valores** e **tipos**

**<** - Comparação de **menor que**

**>** - Comparação de **maior que**

**<=** - Comparação de **menor que *ou* igual**

**>=** - Comparação de **maior que *ou* igual**

```javascript
"1" == 1 // true
"1" === 1 // false
"1" != 1 // false
"1" !=== 1 // true
3 < 2 // false
3 > 2 // true
3 <= 3 // true
3 >= 3 // true
```

 Essas comparações foram feitas utilizando dos **valores** e até **tipos** das variáveis/constantes, entretato, há casos em que a comparação utiliza do **endereço de memória** (número único que define a variável/constante) da variável/constante para a comparação, causando assim, um resultado inesperado

```javascript
const d1 = new Date(0)
const d2 = new Date(0)

d1 == d2 // false
d1 === d2 // false
```

No exemplo acima, a variável/constante armazena uma **referência do endereço de memória**, que é único para cada variável/constante, por isso o false em ambas as comparações

A forma de resolver isso seria obtendo o **valor** e usando ele na comparação

```javascript
d1.getTime() == d2.getTime() // true
d1.getTime() === d2.getTime() // true
```

