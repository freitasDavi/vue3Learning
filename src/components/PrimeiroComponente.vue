<template>
    <div>
        <h1>Olá vue!</h1>
        <p>Meu nome é {{ nome }} e trabalho como {{ profissao }} </p>
        <MultiplosEventos />
    </div>
</template>

<script>
    import MultiplosEventos from './MultiplosEventos.vue';

export default {
    name: 'PrimeiroComponente',  
    data () {
        return {
            nome: "Davi",
            profissao: "Programador"
        }
    },
    components: {
        MultiplosEventos
    }
};
</script>
