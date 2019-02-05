# Javascript - Estrutrura de Controle IF

##### A estrutura do **If**

```javascript
if (/*condição*/){
    // Código
}
```

Caso seja passado apenas uma variável como "condição", ela será automaticamente convertida para um valor *boolean*

Caso dentro do bloco do **if** tenha apenas **uma sentença de código**, é possível omitir as { }

```javascript
if (/*condição*/)
	// Código
 // Essa linha já não faz mais parte do if()
```

Apesar dessa possibilidade, não é uma boa prática



---

##### A estrutura do **if/else**

```javascript
if (/*condição*/){
    // Código
}else{
    // Código
}
```

O código só toma o rumo do **else** quando a condição é **false** (falsa)



---

##### A estrutura do **if/else-if/else**

```javascript
if (/*condição*/){
    // Código
}else if (/*condição*/){
    // Código
}else{
    // Código
}
```

O código só irá para o segundo **if** caso o primeiro retorne **false** (falso) 



---

