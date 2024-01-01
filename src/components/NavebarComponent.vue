<template>
  <div class="navbar">
    <nav class="navbar navbar-expand-lg bg-light">
      <div class="container-fluid">
        <a class="navbar-brand" href="#">
          <img src="../assets/img/d’Perfume.png" alt="logo" />
        </a>
        <div class="nav-cart d-lg-none"> 
          <span class="material-symbols-outlined">shopping_cart</span>
          <span class="cart-num">3</span>
        </div>
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
              <router-link
                to="/product"
                class="list-group-item list-group-item-action"
                aria-current="true"
              >
                <span class="material-symbols-outlined d-none d-lg-block">store</span>
                <span>Product</span>
              </router-link>
            </li>

            <li class="nav-item d-none d-lg-block">
              <router-link
                to="/"
                class="list-group-item list-group-item-action"
                aria-current="true"
              >
              <span class="material-symbols-outlined d-none d-lg-block">person</span>
              <span>log in</span>
            </router-link>
            </li>
            <li class="nav-item d-lg-block">
              <router-link
                to="/wishList"
                class="list-group-item list-group-item-action"
                aria-current="true"
              >
              <span class="material-symbols-outlined d-none d-lg-block">favorite</span>
              <span> Wishlist</span>
            </router-link>
            </li>
            <li class="nav-item d-block d-lg-none">
              <router-link
                to="/"
                class="list-group-item list-group-item-action"
                aria-current="true"
              >
              <span> Blog</span>
            </router-link>
            </li>
            <li class="nav-item d-block d-lg-none">
              <router-link
                to="/"
                class="list-group-item list-group-item-action"
                aria-current="true"
              >
              <span> Contact</span>
            </router-link>
            </li>

            <li class="nav-item d-none d-lg-block">
              <router-link
                to="/"
                class="list-group-item list-group-item-action"
                aria-current="true"
              >
              <span class="material-symbols-outlined">shopping_cart</span>
              <span>Cart(3)</span>
            </router-link>
            </li>
            <li class="nav-item d-block d-lg-none">
              <router-link
                to="/"
                class="list-group-item list-group-item-action"
                aria-current="true"
              >
              <span> log in</span>
            </router-link>
            </li>
          </ul>
        </div>
      </div>
    </nav>
  </div>
</template>
<script></script>
<style lang="scss">
@import '../assets/navebarComponent.scss';
</style>
