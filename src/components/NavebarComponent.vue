<template>
  <div class="navbar">
    <nav class="navbar navbar-expand-lg bg-light">
      <div class="container-fluid">
        <a class="navbar-brand" href="#">
          <img src="../assets/img/d’Perfume.png" alt="logo" />
        </a>
        <button
          class="navbar-toggler"
          type="button"
          data-bs-toggle="collapse"
          data-bs-target="#navbarSupportedContent"
          aria-controls="navbarSupportedContent"
          aria-expanded="false"
          aria-label="Toggle navigation"
        >
          <span class="navbar-toggler-icon"></span>
        </button>

        <div class="collapse navbar-collapse" id="navbarSupportedContent">
          <ul class="navbar-nav me-auto mb-2 mb-lg-0">
            <li class="nav-item">
              <span class="material-symbols-outlined d-none d-lg-block">store</span>
              <span>Product</span>
            </li>
            <li class="nav-item d-none d-lg-block">
              <span class="material-symbols-outlined d-none d-lg-block">person</span>
              <span>log in</span>
            </li>
            <li class="nav-item  d-lg-block">
              <span class="material-symbols-outlined d-none d-lg-block">favorite</span>
              <span> Wishlist</span>  
            </li> 
            <li class="nav-item d-block d-lg-none">             
              <span> Blog</span>  
            </li> 
            <li class="nav-item d-block d-lg-none">             
              <span> Contact</span>  
            </li>                
  
            <li class="nav-item d-none d-lg-block">
              <span class="material-symbols-outlined">shopping_cart</span>
              <span>Cart(3)</span>  
            </li>
            <li class="nav-item d-block d-lg-none">             
              <span> log in</span>  
            </li> 
           
          </ul>
          
        </div>
      </div>
    </nav>
  </div>
</template>
<script>

</script>
<style lang="scss">
@import '../assets/navebarComponent.scss';
</style>
