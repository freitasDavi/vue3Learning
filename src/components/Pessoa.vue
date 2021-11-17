<template>
    <div>
        <h2>Essa é a descrição da pessoa: {{ nome }}</h2>
        <Info :email="email" :esta_trabalhando=false />
        <Form />
    </div>
</template>

<script>
    import Info from "./Info.vue";
    import Form from './Form.vue';

    export default {
        name: 'Pessoa',
        data () {
            return {
                nome: "Davi",
                email: "davi3@mail.com"
            }
        },
        components: {
            Info,
            Form
        }
    }
</script>
