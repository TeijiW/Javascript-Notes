# Javascript - Funções Factory

> Uma **Função *Factory*** é uma função que sempre retorna um objeto



A estrutura de uma **Função Factory**

```javascript
function funçãoFactory(Parâmetro1, Parâmetro2, ...){
    return {
        chave1: Parâmetro1,
        chave2: Parâmetro2,
        chave3: valorFixo,
    }
}

const objeto = funçãoFactory(Parâmetro1, Parâmetro2, ...)
```

