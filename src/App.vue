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
  <div>
    <NavebarComponent></NavebarComponent>    
  </div> 
  <RouterView />
</template>

<style lang="scss">
@import "./assets/all.scss";
#app{
  margin: 0 !important;
  padding: 0 !important;  
 
}

</style>
