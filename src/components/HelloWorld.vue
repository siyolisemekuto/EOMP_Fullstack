<template>
  <div class="hello">
    <img :src="imgUrl" v-on:mouseover="mouseover" v-on:mouseleave="mouseleave" />
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  
  data () {
    return{
      imgUrl: "https://i.postimg.cc/pLyCyBVq/wallpaper.jpg"
    }
  }, 
  methods: {
    mouseover(){
      this.imgUrl = "https://i.postimg.cc/yYk3V2Nr/lucas-mendes-Cyfm-Spq-NMD8-unsplash.jpg"
    },    
    mouseleave(){
      this.imgUrl = "https://i.postimg.cc/pLyCyBVq/wallpaper.jpg"
    }
  },
}


</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
img{
  width:100vw;
  height:90vh;
  object-fit:cover;
}
</style>
