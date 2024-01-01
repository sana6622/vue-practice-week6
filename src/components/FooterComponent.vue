<template>
  <div class="footer">
    <div class="footer-subscription">
      <div class="main">
        <p>記得</p>
        <p>訂閱以獲取更多資訊！</p>
        <div class="search">
          <input type="text"  placeholder="Your email address">
          <button type="button"> Subscribe</button>
        </div>        
      </div>
    </div>

    <div class="footer-bar">
      <div class="bar-img">
        <img src="../assets/img/d’Perfumewhite.png" alt="logo" />
      </div>
      <p>©2020. All Rights Reserved.</p>
      <ul class="d-none d-lg-flex">
        <li>
          <router-link
            to="/product"
            class="list-group-item list-group-item-action"
            aria-current="true"
            >Product
          </router-link>
        </li>
        <li>
          <router-link to="/" class="list-group-item list-group-item-action" aria-current="true"
            >Blog
          </router-link>
        </li>
        <li>
          <router-link
            to="/"
            class="list-group-item list-group-item-action"
            aria-current="true"
          >
            Contact
          </router-link>
        </li>
      </ul>
    </div>
  </div>
</template>
<script></script>
<style lang="scss">
@import '../assets/footer.scss';
</style>
