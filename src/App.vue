<template>
  <div class="container">
    <h1 class="text-center my-3">API Paises</h1>
    <hr class="w-75 bg-dark">
    <Continentes />
    <Buscador />
    <CardList />
  </div>
</template>

<script>
import CardList from './components/CardList.vue'
import Continentes from './components/Continentes.vue'
import Buscador from './components/Buscador.vue'
export default {
  name: 'App',
  components: {
    CardList,
    Continentes,
    Buscador
  }
}
</script>

<style>

</style>
