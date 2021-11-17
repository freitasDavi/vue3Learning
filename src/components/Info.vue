<template>
    <div>
        <p v-if="esta_trabalhando">Estou trabalhando no momento.</p>
        <p v-else>Estou em busca de novas oportunidades</p>
        <p>Utilizo as seguintes tecnologias: </p>
        <ul>
            <li>Javascript</li>
            <li>PHP</li>
            <li>Python</li>
        </ul>
        <div>
            <button @click="showEmail" > {{text_botao}} </button>
        </div>
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
        data () {
            return {
                esta_trabalhando: false,
                mostrar_email: false,
                email: "davi@gmail.com",
                meu_link: "https://www.google.com",
                text_botao: "Mostrar email"
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