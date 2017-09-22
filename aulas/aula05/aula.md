# Renderizando Condições

Vamos aprender a usar o poder das estruturas condicionais em nossos componentes. As estruturas condicionais estão presentes em nossa vida o tempo inteiro, é quando perguntamos 'se'. Por exemplo: 

Se chover então eu vou ficar em casa, senão eu vou para a rua.

![img02](assets/img02.png)

Vamos analisar um exemplo prático!

```vue
<template>
	<section>
		<div>
			<h2>Time Amarelo</h2>
			<p>{{ timeAmarelo }}</p>
			<div>
				<button v-on:click="addtimeAmarelo()">+</button>
				<button v-on:click="removetimeAmarelo()">-</button>
			</div>
		</div>
		<div>
			<h2>Time Roxo</h2>
			<p>{{ TimeRoxo }}</p>
			<div>
				<button v-on:click="addTimeRoxo()">+</button>
				<button v-on:click="removeTimeRoxo()">-</button>
			</div>
		</div>
		<button v-on:click="mostraGanhador()">Mostrar ganhador</button>
		<p> {{ ganhador }} </p>
	</section>
</template>
```

```vue
<script>
	export default {
		name: 'Duelo',
		data() {
			return {
				timeAmarelo: 0,
				TimeRoxo: 0,
				ganhador: ''
			}
		},
		methods: {
			addtimeAmarelo() {
				return this.timeAmarelo++					
			},
			removetimeAmarelo() {
				return this.timeAmarelo--					
			},
			addTimeRoxo() {
				return this.TimeRoxo++
			},
			removeTimeRoxo() {
				return this.TimeRoxo--					
			}
		}
	}
</script>
```
