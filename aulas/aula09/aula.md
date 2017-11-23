# Consumindo uma API

Vamos falar um pouco da história da web novamente para entendermos como ela funciona hoje. 

Em nosso módulo primeiros passos na web, aprendemos que quando estamos navegando na web, o navegador envia requisições para um servidor e o servidor, por sua vez, nos devolve uma resposta em um formato específico ou realiza alguma ação caso pedirmos.

Quando a web nasceu, ela era usada para interconectar documentos. Hoje temos uma web de dados! Antes precisávamos criar vários arquivos em HTML, e esses arquivos eram servidos em nosso navegador, por muito tempo foi tudo simples assim, e ainda pode ser.

Contudo, atualmente não trocamos mais apenas documentos, agora podemos criar não somente sites, mas também aplicações, e em nessas aplicações precisamos consumir ou ainda gerar dados e mais dados!

A web que conhecemos evoliu muito, e nosso navegador ganhou maiores poderes.

## Métodos HTTP

Muita coisa mudou, mas continuamos fazendo requisições. Nas requisições, especificamos o que chamamos de método HTTP ou verbo, temos vários verbos diferentes. Os principais verbos HTTP são:

- GET: Usamos para pegar algo
- POST: Usamos para enviar algo
- PUT: Usamos para editar algo
- DELETE: Usamos para excluir algo

## Axios

> "Existe uma ferramenta para cada tarefa, e uma tarefa para cada ferramenta."
> – Tywin Lannister, A Storm of Swords

Vamos usar o Axios como ferramenta, o axios é uma biblioteca que usaremos como um cliente HTTP, ele funciona no navegador ou no servidor. Em nosso caso, vamos instalar a biblioteca no nosso projeto.

Lembre-se de usar --save para adicionar essa dependência no package.json 

```bash
npm install axios --save
```

Faremos requisições dentro de nossos próprios componentes para consumir dados de uma API. Há muitas APIs abertas por aí, então não se preocupe ainda se você não tem uma.

Por fins didáticos, preferimos usar uma API falsa para explicar como o Axios funciona. Vamos consumir os dados que vem do [jsonplaceholder](https://jsonplaceholder.typicode.com/).


