# Javascript - Noção de Runtime (Contexto de Execução)

> No **Front-End** se trabalha muito com operações assíncronas



No Runtime de Browser, o escopo global seria o ***window***, ele que todas as variáveis criadas em uma aplicação no Browser

No Node.JS, temos o ***global***, que tem o mesmo efeito do *window*. 

Caso seja criada uma variável/constante com *let* ou *const* , essa não poderá ser acessada por notação ponto pelo *window*, pois ela foi criada num escopo "inferior" ao global

Já no caso de funções e variáveis declaradas com *var*, essas poderão ser acessadas globalmente, com *this.* ou *window.* 

Para o Node.JS, cada arquivo é um *module* diferente

**Não é recomendado** criar uma variável **sem var ou let**, pois neste caso, a variável é colocada no escopo **global**

```javasc
a = 2
```

