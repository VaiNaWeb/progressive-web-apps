# Renderizando Condições e Listas

Vamos aprender a usar o poder das estruturas condicionais em nossos componentes.

![img01](assets/img01.png)
```vue
<template>
  <div>
    <button>olá baby</button>
    <div>
    	<img src="https://s-media-cache-ak0.pinimg.com/736x/ca/c7/4d/cac74dc6a46078579bc13cf77c30abf7--baby-no-facebook.jpg">
    	<p>é a mamãe</p>
    </div>
    <div>
    	<img src="https://i.pinimg.com/736x/bf/5c/cc/bf5cccadb664bd703f4b72a0df5a9515--meme-baby.jpg">
    	<p>não é a mamãe</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Aula04',
  data () {
    return {
      mae: true
    }
  }
}
</script>
```

```vue
<template>
  <div>
    <button v-on:click="mae = !mae">olá baby</button>
    <div v-if="mae">
    	<img src="https://s-media-cache-ak0.pinimg.com/736x/ca/c7/4d/cac74dc6a46078579bc13cf77c30abf7--baby-no-facebook.jpg">
    	<p>é a mamãe</p>
    </div>
    <div v-else> 
    	<img src="https://i.pinimg.com/736x/bf/5c/cc/bf5cccadb664bd703f4b72a0df5a9515--meme-baby.jpg">
    	<p>não é a mamãe</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Aula04',
  data () {
    return {
      mae: true
    }
  }
}
</script>
```

![img04](assets/img02.gif)