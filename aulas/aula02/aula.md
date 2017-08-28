# Começando com VUE

> "Eu sempre fiz algo que eu estava pouco preparada para fazer. Eu acho que é assim que você cresce. Quando há aquele momento de 'Wow, não tenho certeza de que posso fazer isso', e você passa por esses momentos, é quando você tem um avanço."
> — Marissa Mayer

Como aprendemos anteriormente, uma interface pode e deve ser divida em vários componentes. Vamos começar a criar nossos primeiros componentes usando o Vue.js.

## Tudo numa coisa só

O Vue trabalha na estrutura de HTML, CSS e JS em um único arquivo, chamamos isso de **Single file components**, o componente inteiro em um arquivo.

Um componente em Vue se divide em três tags, a template, script, e style. Dentro da tag template é onde colocamos o HTML normal que já conhecemos, divs, headers, parágrafos, etc. Dentro de script colocamos o javascript. E por fim, em style colocamos o nosso CSS.

```vue
<template>
  <div id="olaMundo">
    <img src="./assets/logo.png">
    <h1>{{ texto }}</h1>
  </div>
</template>

<script>
export default {
  name: 'olaMundo',
  data () {
    return {
      texto: 'Olá mundo'
    }
  }
}
</script>

<style>
  #olaMundo {
    padding: 5em;
  }
  img {
    max-width: 20%;
  }
  h1 {
    font-family: Helvetica, Arial, sans-serif;
    color: #2c3e50;
  }
</style>
```

![olavue](assets/01.png)


## Criando listas
