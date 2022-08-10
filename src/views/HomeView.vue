<template>
  <div class="home">
   
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'HomeView',
  components: {
    HelloWorld
}
}
</script>

<style scope>
.home{
  /* background-size:100%; */
  background-image:url('https://i.postimg.cc/pLyCyBVq/wallpaper.jpg');
  /* background-color:#cccccc; */
  background-repeat:no-repeat;
  height:90vh;
  /* align-items:center; */
}
</style>
