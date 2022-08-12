<template>
<div class="card-display">
<Catalogue v-for="product in products" :key="product.id" :product="product"/>
</div>
</template>

<script>
import Catalogue from "../components/Catalogue.vue"
export default {
  components:{Catalogue},
    data(){
      return{
        products:[],
      };
    },
    mounted(){
      fetch("http://localhost:6969/products")
      .then((res)=> res.json())
      .then((data) => (this.products = data))
      .catch(err => console.log (err.message))
    }
}
</script>
<style lang="">
    
</style>