<template>
  <div class="contato">
    <h3 class="contato__title">{{ titulo }}</h3>
    <input 
      type="email"
      class="contato__in"
      placeholder="ingrese email">
    <input 
      type="text"
      class="contato__in"
      placeholder="ingrese mensaje">
    
    <button class="contato__btn">Enviar</button>
  </div>
</template>

<script>
  export default {
    name: 'ContactoCursos',
    props: {
      titulo: String
    }
  }
</script>

<style lang="scss" scoped>
  .contato {
    border: 1px solid;
    display: block;
    &__title {
      font-size: 15px;
      font-weight: bold;
    }
    &__in {
      display: block;
      height: 35px;
      margin: 10px;
    }
    &__btn {
      margin: 10px;
      padding: 7px 16px 7px 16px;
    }
  }
</style>