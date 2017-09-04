# Eventos e Métodos

Há muitos eventos que acontecem em nossa página, como eventos do mouse, eventos do teclado, etc. E podemos manipula-los conforme nossas necessidades.

Mais uma diretiva bem legal do Vue é a [v-on](https://br.vuejs.org/v2/guide/events.html#Escutando-Eventos), podemos usa-la para escutar os [eventos](https://pt.khanacademy.org/computing/computer-programming/html-css-js/html-js-dom-events/a/dom-event-types) do DOM em nossa página e adicionar alguma modificação quando eventos forem chamados. Exemplo:

Queremos escutar o evento Click do mouse em um botão, então adicionamos dentro da tag desse botão a diretiva v-on:click. 

```vue
<template>
  <div class="ola">
    <button v-on:click>{{frase}}</button>
  </div>
</template>

<script>
export default {
  name: 'Aula04',
  data () {
    return {
      frase: 'clique em mim!'
    }
  }
}
</script>
```
![img01](assets/img01.png)

Já adicionamos nossa diretiva, mas não tinhamos feito nada com ela ainda. Agora vamos fazer isso! Vamos alterar o valor da nossa variável frase, quando o evento click for chamado vamos alterar esssa frase.

```vue
<template>
  <div class="ola">
    <button v-on:click="frase = 'Olá mundo'">{{frase}}</button>
  </div>
</template>

<script>
export default {
  name: 'Aula04',
  data () {
    return {
      frase: 'clique em mim!'
    }
  }
}
</script>
```
![img02](assets/img02.gif)
