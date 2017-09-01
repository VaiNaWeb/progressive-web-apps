# Começando com VUE

- Vue trabalha na estrutura de HTML, CSS e JS em um único arquivo, chamamos isso de Single file components, o componente inteiro em um arquivo.
- Um componente em Vue se divide em três tags: template, script, e style. Dentro da tag template é onde colocamos o HTML normal que já conhecemos, divs, headers, parágrafos, etc. Dentro de script colocamos o javascript. E por fim, em style colocamos o nosso CSS.
- Podemos usar um atributo em style chamado scoped, se usarmos, os estilos declarados no componente estilizam somente esse componente, o que pode ser bem útil em grandes aplicações.
- Dentro do template podemos usar a sintaxe mustache, {{ duas chaves }}, e colocar expressões em Javascript. Criamos um mustache com uma varíável chamada mensagem e atribuímos a ela uma frase. 
- Você pode entender uma variável como um espacinho na memória reservado a guardar alguma coisa, algo como reservar um espaço em um armário para guardar futuramente alguma coisa.
- Nossos dados estão ligados. O que acontece dentro de template reflete também no script, e o que acontece no Javsacript também reflete no template.
- O vue tem algumas palavras reservadas chamadas de Diretivas que nos permitem adicionar alguns comportamentos. Uma dessas diretivas é a v-model, vamos usa-la para criar um two-way data binidng, ou ligação de dados por dois caminhos em um elemento.
- O v-model é semelhante a outros atributos comuns que usamos no HTML, um exemplo: adicionamos como valor nesse atributo a nossa variável, depois usamos um mustache com a mesma variável para mostrar o que o usuário digitou em nosso input.
