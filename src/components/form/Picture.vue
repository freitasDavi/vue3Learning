<template>
    <img  :src="avatar" :alt="descricao" >
  <MudarImagem @papo-reto="trocarImagem" />
</template>

<script>
    import MudarImagem from "@/components/MudarImagem";
    export default {
      name: "Picture",
      components: {
          MudarImagem
      },
      data () {
            return {
                avatar: "/img/avatar.png",
                descricao: "Usuario"
            }
      },
      methods: {
        trocarImagem() {
          this.avatar = "/img/avatar2.jpg"
        }
      }
    }
</script>