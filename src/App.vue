<template>
  <div id="app">

    <!-- <router-link :to="{path: '/'}">Home</router-link>
    <router-link :to="{path: '/test/1'}">Test 1</router-link>
    <router-link :to="{path: '/test/2'}">Test 2</router-link>
    <router-link :to="{path: '/test/3'}">Test 3</router-link>

     -->

    <navbar @search="search"></navbar>

    <div class="container">
      <div class="row">
        <div class="col-sm-9">
          <router-view></router-view>
          <!-- <inventory @newCartItem="addToCartItem" :items="items"></inventory> -->
        </div>
        <div class="col-sm-3">
          <cart @itemRemoved="removeCartItem" :items="cart"></cart>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Navbar from "./components/Navbar"
// import Inventory from "./components/Inventory";
import Cart from "./components/Cart";
import data from "./data";

export default {
  components:{
    Navbar,
    // Inventory,
    Cart
  },
  data() {
    return{
      items: [],
      cart: []
    }
  },
  mounted() {
    this.items = data
  },
  methods: {
    search(keyword){
      this.items = data.filter(item => {
        return item.title.toLowerCase().indexOf(keyword.toLowerCase()) !== -1
      })
    },
    addToCartItem(item){
      this.cart.push(item)
    },
    removeCartItem(index){
      this.cart.splice(index,1)
    }
  }
}
</script>

<style>
  .container{
    padding-top: 10px;
  }
</style>
