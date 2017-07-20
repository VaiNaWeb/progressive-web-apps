# Olá Vue

Vamos criar nossos primeiros componentes usando o Vue.js.

## Tudo numa coisa só

O Vue trabalha com o conceito de Single file components, o HTML, CSS e JS ficam separados mas em um único arquivo.

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

## Criando listas
