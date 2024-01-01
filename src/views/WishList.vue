<template>
    <div class="product">
      <div class="sub-nav">
        <ul>
          <li>CHANEL</li>
          <li>Jo Malone</li>
          <li>Curology</li>
          <li>Dior</li>
          <li>Chloe</li>
          <li>ZARA</li>
        </ul>
      </div>
      <ul class="list">
        <li v-for="(item, index) in datas" :key="index">
          <div class="list-img">
            <img :src="item.image" alt="image" />
          </div>
          <h3>{{ item.title }}</h3>
          <p>{{ item.category }}</p>
          <div class="list-prices">
            <span>NT{{ item.price }}</span>
            <span class="sp-price">NT{{ item.origin_price }}</span>
          </div>
          <div class="list-icons">
          <div v-if="!item.isLike" class="unfill">
          <span
            v-if="!item.isLike"
            class="material-symbols-outlined"
            v-on:click="clickFavorite(item.id)"
            >favorite</span
          >
          </div>
          <div v-else class="fill">
            <span  class="fill material-symbols-outlined" v-on:click="clickFavorite(item.id)"
            >favorite</span
          >
          </div>
          <div class="unfill">
            <span class="material-symbols-outlined">shopping_cart</span>
          </div>         
        </div>
        </li>
      </ul>
    </div>
  </template>
  <script>
  export default {
    data() {
      return {
        datas: {},
        favorite: []
      }
    },
    mounted() {
      this.getData()
    },
  
    methods: {
  
      getData() {
        this.favorite = JSON.parse(localStorage.getItem('favorite'))
        // console.log('env', import.meta.env.VITE_PATH)
        // console.log('env text ', import.meta.env.VITE_TEXT)
        const url = import.meta.env.VITE_PATH
        this.$http.get(url).then((res) => {
          this.datas = res.data.products
        //   console.log('this.data', this.datas)
          this.datas = this.datas.map((el) => {
            return { ...el, isLike: false }
          })
          this.favorite.forEach(id=>{
            this.datas.forEach(data=>{
              if(data.id===id){
                data.isLike=true
              }
            })
          })
          this.datas=this.datas.filter(item=>{
            return item.isLike==true
          })
        })
      },
  
      clickFavorite(id) {
        this.favorite = JSON.parse(localStorage.getItem('favorite'))
       
        if (this.favorite != null) {
          const check = this.favorite.findIndex((el) => {
            return el === id
          })        
          if (check!=-1) {
            this.favorite.splice(check,1)
            // console.log('有相符的', this.favorite)
          } else {
            this.favorite.push(id)
            // console.log('沒有相符的', this.favorite)
          }
        } else {
          this.favorite = [id]
        }
  
        this.datas.find((item) => {
          if (item.id === id) {          
            item.isLike = !item.isLike          
          }
        })
        this.datas=this.datas.filter(item=>{
            return item.isLike==true
          })       
     
        localStorage.setItem('favorite', JSON.stringify(this.favorite))
      }
    }
  }
  </script>
  
  <style lang="scss">
  @import '../assets/productView.scss';
  </style>
  