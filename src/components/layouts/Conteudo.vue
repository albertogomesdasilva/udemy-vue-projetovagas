<template>
    <div>
   <h1>{{ titulo }}</h1>
   <!-- <button @click="atualizarConteudo">Atualizar</button> -->
   <button @click="conteudo = 'home'">Home</button>
   <button @click="conteudo = 'publicar-vaga'">Publicar Vaga</button>
  
    <!-- <home></home>
    <publicar-vaga></publicar-vaga> -->
    <keep-alive>

        <component :is="conteudo" />
    </keep-alive>
</div>
</template>

<script>
    import Home from '@/components/views/Home.vue'
    import PublicarVaga from '@/components/views/PublicarVaga.vue';
    export default {
        name: 'Conteudo',

        components: {
            Home,
            PublicarVaga
        }, 
        data: () => ({
            titulo: 'Componente Conteúdo',
            conteudo: 'home'
        }),
        methods: {
            atualizarConteudo() {
                this.titulo += '*'
            }
        }
    }


</script>

<style scoped>
  
</style>


