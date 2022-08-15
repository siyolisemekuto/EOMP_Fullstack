<template>
    <div>
      <h1>This is a cart</h1>
      <div @mouseover=true class="cards">
  <img :src="product.image" alt="product image">
  <h1>{{product.name}}</h1>
            <p>{{product.description}}</p>
            <p>{{product.price}}</p>
        </div>   
    </div>
</template>


<script>
export default {
    computed: {
        products() {
            return this.$store.state.products;
       }
  },
  mounted() {
    this.$store.dispatch('fetchProducts');
  }
}
</script>
<style scoped>
    h1{
        font-size:41em;
    }
</style>