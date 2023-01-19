<template>
  <div>
  <AppHeader></AppHeader>
  <router-view></router-view>
  <h1>Za Warudo</h1>
  </div>
</template>

<script>
import AppHeader from './components/HeaderComponent.vue';
  export default {
    name: 'App',
    components:{
      AppHeader
    }
  }
</script>

<style lang="scss" scoped>

</style>