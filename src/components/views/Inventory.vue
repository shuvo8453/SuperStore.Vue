<template>
  <div v-if="!loading" class="row">
    <div v-for="(item, index) in items" :key="index" class="card m-2" style="width: 18rem;">
      <img class="card-img-top" :src="item.photo" alt="Card image cap">
      <div class="card-body">
        <h5 class="card-title">{{ item.title }}</h5>
        <p class="card-text">{{ item.price }}</p>
        <a @click="addCartItem(item)" class="btn btn-primary">+add</a>
      </div>
    </div>
  </div>
  <h1 v-else> Loading... </h1>
</template>

<script>
import axios from 'axios'

export default {
  data() {
    return {
      loading: true,
      items  : []
    }
  },
  mounted() {
    this.fetchInventory()
  },
  methods: {
    addCartItem(item) {
      this.$emit("newCartItem", item)
    },
    fetchInventory() {
      let self = this
      axios.get('http://api_server.test/api/data').then(response => {
        self.items   = response.data
        self.loading = false
      })
    }
  },
}
</script>

<style>

</style>