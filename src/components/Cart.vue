<template>
  <ul class="list-group mt-4">
    <li class="list-group-item">
      <span class="item-name">Name</span>
      <span class="item-price float-right">Price</span>
    </li>
    <hr>
    <li v-for="(item, index) in items" :key="index" class="list-group-item">
      <button @click="removeItem(index)" class="btn btn-sm btn-danger">-</button>
      <span class="item-name">{{ item.title }}</span>
      <span class="item-price float-right">{{ item.price  }}</span>
    </li>
    <li class="list-group-item">
      <span class="item-name">Total</span>
      <span class="item-price float-right">${{ totalPrice }}</span>
    </li>
  </ul>
</template>

<script>
export default {
  props: ['items'],
  computed:{
    totalPrice(){
      let total = 0;
      this.items.forEach(item => {
        total += parseFloat(item.price.split("$")[1])
      })
      return parseFloat(total.toFixed(2))
    }
  },
  methods:{
    removeItem(index){
      this.$emit('itemRemoved', index)
    }
  }
}
</script>

<style>

</style>