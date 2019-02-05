# Javascript - Declaração de variável com var

> Ou uma variável com var tem escobo **global** ou tem escopo **de função**

> Uma variável declarada com var sofre o **hoisting** (*Içamento*)



O **hoisting** (*içamento*) é o ato da declaração de uma variável ser "movida" para o topo

```javascript
console.log(a) // undefined
var a = 20
console.log(a) // 20
```



Variáveis declaradas com **var** são  "globais" quando declaradas em blocos *não especiais* (blocos sem conteúdo)

```javascript
{
    {
        {
            var a = 20
        }
    }
}
console.log(a) // 20
```



---

Variáveis declaradas com **var** em blocos de função se restrigem apenas a esses blocos

```javascript
function teste(){
    aa = 123
}
console.log(aa) // Erro!
```

