<template>
    <div>
        <button @click="primeiro(txt1, $event), segundo(txt2, $event), terceiro()">Ativar múltiplos eventos</button>
        <p>{{ multiplosEventos }}</p>
    </div>
</template>

<script>
export default  {
    name: 'MultiplosEventos',
    data () {
        return {
            multiplosEventos: "",
            txt1: "Primeiro evento ",
            txt2: "Segundo evento "
        }
    },
    methods: {
        primeiro(text, e) {
            this.multiplosEventos = text + "ativado"
        },
        segundo(text, e) {
            setTimeout(() => {
                this.multiplosEventos = text + "ativado"
            }, 500);
        },
        terceiro() {
            setTimeout(() => {
                this.multiplosEventos = ""
            }, 1500);
        }
    }
}
</script>

<style scoped>
    div {
        margin: 100px;
    }
</style>

