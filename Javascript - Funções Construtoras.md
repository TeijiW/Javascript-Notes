# Javascript - Funções Construtoras

> É uma função que exerce o papel de uma classe, podendo ser usada para instanciar um objeto

```javascript
function funçãoConstrutora(Parâmetro1, Parâmetro2, ...){
	let atributo1 = x //Atributo privado
	
	this.método1 = function(){ //Método Público
        // Código
	}
}

const objeto1 = new funçãoConstrutora() // Função
const objeto1 = new funçãoConstrutora // Objeto
```

Como visto acima, para criar um método que possa ser acessado publicamente, ele deve ser declarado com ***this***