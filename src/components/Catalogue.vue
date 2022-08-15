<template>
    <div>
        <h1>This is a catalogue</h1>
        <div v-for="product of products" class="cards" >
            <img :src="product.imgUrl" alt="product image">
            <h1>{{product.title}}</h1>
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