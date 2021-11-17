<template>
    <form action="" @submit="enviarFormulario($event)">
        <div>
            <input type="text" v-model="name" >
        </div>
        <div>
            <input type="text" v-model="email">
        </div>
        <div>
            <Submit />
        </div>
        <p>-----</p>
        <p>-----</p>
        <p>-----</p>
    </form>
</template>

<script>
    import Submit from './form/Submit.vue';
    import InputText from './form/InputText.vue';

    export default {
        name: "Form",
        components: {
            InputText,
            Submit
        },
        data () {
            return {
                name: "",
                email: ""
            }
        },
        methods: {
            enviarFormulario (e) {
                e.preventDefault();

                const name = this.name;
                const email = this.email;

                console.log("formulário enviado");
                console.log(`O nome é ${name}, e o email é ${email}`);
            }
        }
    }
</script>

<style scoped>
    p {
        margin: 50px;
    }
</style>