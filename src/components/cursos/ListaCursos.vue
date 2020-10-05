<template>
  <div class="cursos">
    <h3>{{ titulo }}</h3>
    <v-lista 
      :lista="lista"
    />
  </div>
</template>

<script>

  import VLista from '@/components/base/VLista'

  export default {
    name: 'ListaCursos',
    props: {
      titulo: String
    },
    components: {
      VLista
    },
    data() {
      return {
        lista: [
          {id: 0, name: 'Curso profesional de Django'},
          {id: 1, name: 'Curso profesional de Vue'},
          {id: 2, name: 'Curso de introduccion al desarrollo web'},
          {id: 3, name: 'Curso de Adminitrador de Django'},
        ]
      }
    },
  }
</script>

<style lang="scss" scoped>
  .cursos {
    border: 1px solid;
  }
</style>