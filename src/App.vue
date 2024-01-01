<script >
import { RouterLink, RouterView } from 'vue-router'

import NavebarComponent from './components/NavebarComponent.vue';
import Footer from'./components/FooterComponent.vue';
export default{
  components:{    
    NavebarComponent,
    Footer
  }
}
</script>

<template>
  <div>
    <NavebarComponent></NavebarComponent>    
  </div> 
  <RouterView />
  <div>
    <Footer></footer>
  </div>
</template>

<style lang="scss">
@import "./assets/all.scss";
#app{
  margin: 0 !important;
  padding: 0 !important;  
 
}

</style>
