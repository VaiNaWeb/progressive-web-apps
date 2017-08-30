# Introdução

> "Eu não gosto de estudar, eu odeio estudar. Eu gosto de aprender, aprender é lindo."
> — Natalie Portman

Nesse módulo vamos criar **aplicações web progressivas**, vamos chama-las de PWA, com VueJS. As aplicações web progressivas combinam o melhor da Web e o melhor dos aplicativos.

Uma aplicação progressiva, como o próprio nome sugere está mesmo sempre em progresso. Isso quer dizer que ela está sempre ganhando mais recursos e se tornando mais poderosa, assim como a própria web sempre foi.

Comparando como eram feitas as coisas na web logo quando ela foi criada percebemos o quanto ela foi mudando ao longo dos anos, o quanto ela melhorou e continua melhorando de **forma progressiva**. Vale notar também que enquanto ela foi ganhando novos poderes os antigos não pararam de funcionar, esse é um detalhe importante e que tem tudo a ver também com PWA.

Por definição elas precisam ser **confiáveis**, **rápidas**, **engajadoras**. São caractertíscas de uma PWA: 

- **Progressiva** - Funciona para qualquer usuário, em qualquer navegador, é criada com aprimoramento progressivo
- **Responsiva** - Se adequa a diferentes dispositivos
- **Independente de conectividade** - Funciona offline
- **Atual** - Sempre atualizada graças ao processo de atualização do service worker
- **Segura** - Fornecida via HTTPS para evitar invasões
- **Descobrível** - Permite ser encontrada por mecanismos de buscas
- **Re-envolvente** - Facilita o reengajamento com recursos como notificações
- **Instalável** - Permite que os usuários guardem os aplicativos mais úteis em suas telas iniciais sem precisar fazer instalação
- **Linkável** - Compartilhada facilmente por URL

## Javascript

Vamos começar a desbravar o fantástico mundo do **Javascript**, a linguagem de programação mais popular do mundo, muito poderosa e que está em todos os lugares. Podemos encontra-la em robôs, aplicações web, mobile, e em tantas outras coisas, inclusive em seu navegador.

Faça o teste! Clique com o botão direito do mouse em qualquer lugar na tela e pressione Inspecionar elemento ou pressione `(ctrl + shift + i)` e clique em Console.

Digite o comando alert`("Olá mundo");`

O `alert();` é uma função em Javascript, não se preocupe em conhecer o conceito disso agora, ele vai ficar mais claro mais à diante, por enquanto entenda isso como uma ação.

## VueJS

Criada e mantida pela comunidade Open Source. É uma biblioteca em Javascript para construção de **interfaces** com o usuário.

> Uma interface com o usuário é um espaço em que interações entre humanos e máquinas acontecem.
> Wikipedia

Uma interface é divida em **componentes**, e esses componentes se comunicam entre eles. Podemos dividir uma interface em vários componentes, sempre que um componente fica muito complexo devemos começar a pensar em quebra-lo em novos componentes.

Aplicações construídas com Vue possuem interfaces que "reagem" às interações com o usuário, isso quer dizer que se o usuário insere um dado de entrada em um componente por exemplo, esse componente pode mostrar em tempo real uma reação a essa entrada.

Há muitas bibliotecas criadas com a mesma função do Vue, mas ele se destaca pela sua simplicidade.

## Criando um projeto

Vamos usar o Vue-cli, ele nos dá alguns templates para criar a estruta inicial de nossos projetos, enquanto estamos conhecendo o Vue, vamos usar o **webpack**, que possui o Webpack configurado, **vue-router** já estruturado e mais algumas coisas que vão facilitar a nossa vida.

Com tudo instalado corretamente, use o comando para iniciar o projeto:

```bash
vue init webpack MeuProjeto
```

Depois, entre na pasta

```bash
cd MeuProjeto
```

Sempre que iniciamos um novo projeto em nossa máquina, precisamos instalar as dependências dele. Instale as dependências de seu projeto

```bash
npm install
```

Agora já podemos iniciar o projeto

```bash
npm run dev
```

O Vue já criou várias pastas e arquivos para gente, nossos componentes ficam dentro de src/components. Ele criou também um componente chamado Hello.vue, podemos apagar ou editar esse componente, depois criar novos.

Vá em frente! Encontre a frase Welcome to Your Vue.js App na linha 28 e escreva seu próprio Olá mundo. 
