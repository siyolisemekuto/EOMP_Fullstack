<template>
  <div class="home">
   <Login/>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'
import Login from '@/components/Login.vue'

export default {
  name: 'HomeView',
  components: {
    HelloWorld,
    Login
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
