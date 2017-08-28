# Começando com VUE

> "Eu sempre fiz algo que eu estava pouco preparada para fazer. Eu acho que é assim que você cresce. Quando há aquele momento de 'Wow, não tenho certeza de que posso fazer isso', e você passa por esses momentos, é quando você tem um avanço."
> — Marissa Mayer

Como aprendemos anteriormente, uma interface pode e deve ser divida em vários componentes. Vamos começar a criar nossos primeiros componentes usando o Vue.js.

## Criando um projeto

O Vue-cli nos dá alguns templates para criar a estruta inicial de nossos projetos, enquanto estamos conhecendo o Vue, vamos usar o **webpack**, que possui o Webpack configurado, **vue-router** já estruturado e mais algumas coisas que vão facilitar a nossa vida.

Com tudo instalado corretamente, use o comando para iniciar o projeto:

```
vue init webpack MeuProjeto
```

Depois, entre na pasta

```
cd MeuProjeto
```

Sempre que iniciamos um novo projeto em nossa máquina, precisamos instalar as dependências dele. Instale as dependências de seu projeto

```
npm install
```

Agora já podemos iniciar o projeto

```
npm run dev
```


## Tudo numa coisa só

O Vue já criou várias pastas e arquivos para gente, nossos componentes ficam dentro de src/components. Ele criou também um componente chamado Hello.vue, podemos apagar ou editar esse componente, depois criar novos.

Vue trabalha na estrutura de HTML, CSS e JS em um único arquivo, chamamos isso de **Single file components**, o componente inteiro em um arquivo.

Um componente em Vue se divide em três tags: template, script, e style. Dentro da tag template é onde colocamos o HTML normal que já conhecemos, divs, headers, parágrafos, etc. Dentro de script colocamos o javascript. E por fim, em style colocamos o nosso CSS.

Podemos usar um atributo em style chamado scoped, se usarmos, os estilos declarados no componente estilizam somente esse componente, o que pode ser bem útil em grandes aplicações.

```vue
<template>
  <div>
    <p>Olá Mundo</p>
  </div>
</template>

<script>
export default {
  name: 'hello'
}
</script>

<style scoped>
div {
  margin-top: 0.5em;
  padding: 0.25em;
}
p {
  margin: 0;
  padding: 0.25em 0;
  font-size: 1.25em;
}
</style>
```

![olavue](assets/01.png)