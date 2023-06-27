<template>
  <div v-if="item" class="row">
    <div class="col-sm-6">
      <img :src="item.photo" alt="photo">
    </div>
    <div class="col-sm-6">
      <h4>{{ item.title }}</h4>
      <p>{{ item.description }}</p>
      <p>{{ item.price }}</p>
      <a @click="addCartItem(item)" class="btn btn-primary">+add</a>
    </div>
  </div>
  <h3 v-else>Loading...</h3>
</template>

<script>
import axios from "axios";

export default {
  data() {
    return{
      item: null
    }
  },
  mounted() {
    this.fetchItem()
  },
  methods:{
    addCartItem(item) {
      this.$store.commit('addToCart', item)
    },
    fetchItem(){
      axios.get('http://api_server.test/api/data/' + this.$route.params.id).then(response => {
        this.item = response.data.data
      })
    }
  }
}
</script>

<style>

</style>