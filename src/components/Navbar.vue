<template>
  <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
    <router-link :to="{ path:'/' }">
      <a class="navbar-brand">Super Store</a>
    </router-link>
    <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>

    <div class="collapse navbar-collapse" id="navbarSupportedContent">
      <form @submit.prevent="search" class="form-inline my-2 my-lg-0">
        <input class="form-control mr-sm-2" type="search" placeholder="Search"
               aria-label="Search" v-model="keyword">
        <button class="btn btn-outline-success my-2 my-sm-0" type="submit">Search</button>
      </form>
    </div>
  </nav>
</template>

<script>
import axios from "axios";

export default {
  data(){
    return{
      keyword: ''
    }
  },
  methods:{
    search(){
      axios.get('http://api_server.test/api/data?search=' + this.keyword).then(response => {
        this.$store.commit('setInventory', response.data)
      })
    }
  }
}
</script>

<style>

</style>