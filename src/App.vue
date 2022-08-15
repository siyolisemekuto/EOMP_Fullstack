<template>
  <Navbar/>
  <div class="min-vh-100">
    <router-view></router-view>
  </div>
  <!-- <Contact/> -->
  <Footer></Footer>
</template>


<script>
import Navbar from "@/components/Navbar.vue"
import Footer from "@/components/Footer.vue"
// import Contact from "@/components/Contact.vue"

export default {
  components:{
    Navbar,
    Footer
}
}
</script>
<style>
#app {
  font-family: Verdana, Geneva, Tahoma, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  background-color:rgb(250, 249, 246);
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
}
.page{
  background-color:rgb(250, 249, 246);
  height:90vh;
  width:98vw;
}
</style>
