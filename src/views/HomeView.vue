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
