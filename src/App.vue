<template>
  <div>
    <h1>Componente App</h1>
   
    <topoPadrao />
    <conteudo></conteudo>
  </div>
</template>

<script>
import TopoPadrao from '@/components/layouts/TopoPadrao.vue'
import Conteudo from '@/components/layouts/Conteudo.vue'

export default {
  name: 'App',
  components: {
    Conteudo,
    TopoPadrao
  }
}
</script>

<style scoped>
  p {
    color: red
  }
</style>