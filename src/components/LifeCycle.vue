<template>
    <h1>Meu nome é: {{ nome }} </h1>
</template>

<script>
export default {
    name: "LifeCycle",
    data () {
        return {
            nome: "Ainda não sei"
        }
    },
    created () {
        setTimeout(() => {
            this.nome = "Davi"
        }, 1000);

        this.lifeCycle();
    },
    mounted () {
        setTimeout(() => {
            this.nome = "Pedro"
        }, 200);
    },
    methods: {
        lifeCycle() {
            console.log("executou");
        }
    }
}
</script>
