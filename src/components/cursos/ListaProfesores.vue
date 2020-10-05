<template>
  <div class="profesores">
    <h3>{{  titulo }}</h3>
    <v-lista 
      :lista="lista"
    />
  </div>
</template>

<script>
  import VLista from '@/components/base/VLista'

  export default {
    name: 'ListaProfesores',
    props: {
      titulo: String
    },
    components: {
      VLista
    },
    data() {
      return {
        lista: [
          {id: 0, name: 'Cristhian Santa Cruz Carrion'},
          {id: 1, name: 'Neunapp'},
          {id: 2, name: 'cscthian'},
        ]
      }
    },
  }
</script>

<style lang="scss" scoped>

</style>