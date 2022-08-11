<template>
  <div class="hello col-md-6">
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
  width: 40vw;
  height: 68vh;
  margin-right:60px;
  margin-left:60px;
  margin-top: 110px;
  margin-bottom: 20px;
  box-shadow:0 5px 5px 0 rgba(0, 0, 0, 0.2);
  object-fit:cover;
}

</style>
