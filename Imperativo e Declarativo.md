# Imperativo e Declarativo

Na maneira **imperativa**, o foco é em **como fazer** o que é requisitado

```javascript
const alunos = [
	{ nome: "Teiji", nota: 9.5 },
	{ nome: "Eloise", nota: 10.0},
	{ nome: "Fulano", nota: 5.5 }
]

let total1 = 0
for(let i=0; i<alunos.length; i++){
    total1 += alunos[i].nota
}

console.log(total1/alunos.length)
```

Já na maneira **declarativa**, o foco é em **o que fazer**

```javascript
const alunos = [
	{ nome: "Teiji", nota: 9.5 },
	{ nome: "Eloise", nota: 10.0},
	{ nome: "Fulano", nota: 5.5 }
]

const getNota = aluno => aluno.nota // Função que retorna a nota do aluno
const soma = (total, atual) => total+atual // Função do acumulador
const total2 = alunos.map(getNota).reduce(soma)
console.log(total2/alunos.length)
```

