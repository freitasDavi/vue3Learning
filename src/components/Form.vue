<template>
    <form action="">
        <div>
            <Input />
        </div>
        <div>
            <Input />
        </div>
        <div>
            <Submit />
        </div>
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
        }
    }
</script>
