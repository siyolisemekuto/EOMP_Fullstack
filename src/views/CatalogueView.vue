<template>
<h1>This is a catalogue</h1>
<div class="row row-cols-1 row-cols-md-3 g-4">
<div class="col">
  <div class="card" v-for="product of products" >
    <img :src="product.imgURL" class="card-img-top" :alt="product.title">
    <div class="card-body">
      <h5 class="card-title">{{product.title}}</h5>
      <p class="card-text">{{product.description}}</p>
      <p class="card-text"><small>R{{product.price}}</small></p>
    </div>
  </div>
  </div>
  </div>
</template>

<script>
// import Catalogue from '../components/Catalogue.vue'
export default {
  // components:{Catalogue},
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
<style>
  /* .card{
    width:300px;
    display:flex;
  } */
</style>