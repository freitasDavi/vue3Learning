<template>
  <div>
    <button @click="$emit('papoReto')">Trocar imagem de perfil</button>
  </div>
</template>

<script>
export default {
  name: "MudarImagem",
  emits: ['papoReto'],
}
</script>

<style scoped>

</style>