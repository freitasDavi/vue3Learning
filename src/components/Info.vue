<template>
    <div>
        <p v-if="esta_trabalhando">Estou trabalhando no momento.</p>
        <p v-else>Estou em busca de novas oportunidades</p>
        <p>Utilizo as seguintes tecnologias para back-end: </p>
        <ul>
            <li v-for="(technology, index) in backendTechnologies" v-bind:key="index" >{{technology}}</li>
        </ul>
        <div>
            <button @click="showEmail"> {{text_botao}} </button>
        </div>
        <p>Utilizo as seguintes tecnologias para front-end</p>
        <ul>
            <li v-for="(technology) in frontendTechnologies" v-bind:key="technology.id">{{technology.language}}</li>
        </ul>
        <p v-show="mostrar_email">Mande uma mensagem para: {{ email }}</p>
        <p class="teste">Para acessar meu portifolio <a v-bind:href="meu_link" target="blank">basta clicar aqui</a></p>
        <Picture />
    </div>
</template>

<script >
    import Picture from './form/Picture.vue'

    export default {
        name: "Info",
        components: {
            Picture
        },
        props: {
            email: String,
            esta_trabalhando: Boolean
        },
        data () {
            return {
                mostrar_email: false,
                meu_link: "https://www.google.com",
                text_botao: "Mostrar email",
                backendTechnologies: ['javascript', 'php', 'python'],
                frontendTechnologies: [
                    { id: 1, language: 'HTML'},
                    { id: 2, language: 'CSS'},
                    { id: 3, language: 'VUEJS'},
                ]
            }
        },
        methods: {
            showEmail() {
                this.mostrar_email = !this.mostrar_email;
                if(this.mostrar_email) {
                    this.text_botao="Esconder email"
                } else {
                    this.text_botao = "Mostrar email"
                }
            }
        }
    }

</script>

<style>
    .paragrafo-pai {
        color: red;
    }
</style>