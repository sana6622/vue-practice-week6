<script >
import { RouterLink, RouterView } from 'vue-router'

import NavebarComponent from './components/NavebarComponent.vue';
export default{
  components:{    
    NavebarComponent
  }
}
</script>

<template>
  <div class="container">
    <NavebarComponent></NavebarComponent>    
  </div>

  <RouterView />
</template>

<style lang="scss">
@import "./assets/all.scss";

</style>
