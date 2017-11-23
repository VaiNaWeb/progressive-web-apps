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

Dentro da tag script, fora do export, vamos importar a biblioteca:

```vue
<script>
import axios from 'axios';

export default {
  name: 'hello'
}
</script>
```
Depois, é só chamar a requisição, vamos fazer isso dentro de um created(), essa estrutura que estamos usando se chama [promise](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/Promise). Uma promessa, que representa um valor que pode estar disponível.

Por fins didáticos, por enquanto vamos usar uma API falsa para explicar como o Axios funciona. Vamos consumir os dados que vem do [jsonplaceholder](https://jsonplaceholder.typicode.com/).
 
Nossa requisição retornará um [JSON](https://pt.wikipedia.org/wiki/JSON), essa é uma das melhores formas de trabalhar com dados na web, que vem de um endpoint do jsonplaceholder.

Dentro de axios.get() vamos colocar o endpoint que queremos, um endpoint é uma URL onde seu serviço pode ser acessado por uma aplicação.

Para guardar essese valores, vamos criar também um array vazio no data, depois disso, já estamos recebendo os dados e podemos usar facilmente no componente.

```vue
<script>
import axios from 'axios';
export default {
  name: 'hello',
  data () {
    return {
      respostas: [],
    }
  },
  created() {
    axios.get(`http://jsonplaceholder.typicode.com/users`)
    .then(response => {
      this.respostas = response.data
    })
  }
}
</script>
```

Vou assumir que você está usando a extensão do VUE no navegador, e sabe que é hora de ver como esses dados estão chegando no data e ver quais propriedades estão disponíveis. Se não sabia, pois saiba que é isso mesmo, use suas ferramentas ao seu favor.

Duas propriedades que vieram em nosso JSON são o name e o email. Vamos criar um v-for e exibir essas informações!

```vue
<template>
  <section>
    <ul>
      <li v-for="resposta in respostas">
        <p><strong>{{resposta.name}}</strong></p>
        <p>{{resposta.email}}</p>
      </li>
    </ul>
  </section>
</template>
```
