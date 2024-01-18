<script >
import MainComp from './components/MainComp.vue';
export default {
  name: 'app',
  components: {
    MainComp
  }
}
</script>

<template>
  <h1>Ciao mondo</h1>
  <MainComp></MainComp>
</template>

<style lang="scss">
@use './style/main.scss';
</style>
