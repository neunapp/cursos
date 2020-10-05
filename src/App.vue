<template>
  <div class="header">
    <h3 class="header__title">Nuenapp Cursos</h3>
    <ul class="header__lista">
      <li class="header__lista__item">
        <a 
          @click="mostrarComponente('lista-cursos', 'Lista de cursos')"
          class="header__lista__item__link">
            Cursos
        </a>
      </li>
      <li class="header__lista__item">
        <a 
          @click="mostrarComponente('lista-profesores', 'Lista Profesores')" 
          class="header__lista__item__link">
            Profesores
        </a>
      </li>
      <li class="header__lista__item">
        <a 
          @click="mostrarComponente('contacto-cursos', 'Formulario de contacto')"
          class="header__lista__item__link">
            Contacto
        </a>
      </li>
    </ul>
  </div>
  <keep-alive>
    <component 
      :is="componentSelect"
      :titulo="propComponent" 
    />
  </keep-alive>
</template>

<script>

  import ListaCursos from '@/components/cursos/ListaCursos'
  import ListaProfesores from '@/components/cursos/ListaProfesores'
  import ContactoCursos from '@/components/cursos/ContactoCursos'

  export default {
    name: 'App',
    data() {
      return {
        componentSelect: null,
        propComponent: ''
      }
    },
    components: {
      ListaCursos,
      ListaProfesores,
      ContactoCursos
    },
    methods: {
      mostrarComponente: function (componente, propiedad) {
        this.componentSelect = componente
        this.propComponent = propiedad
      }
    }
  }
</script>

<style lang="scss">
* {
  margin: 0px;
  padding: 0px;
}
.header {
  padding: 1em;
  border: 1px solid;
  display: flex;
  justify-content: space-between;
  align-items: center;
  &__lista {
    display: flex;
    list-style: none;
    padding: 0px;
    margin: 0px;
    &__item {
      padding: 1em;
    }
  }
}
</style>
