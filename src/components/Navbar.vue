<template>
    <header :class="{'scrolled-nav':scrollPosition}">
    <nav class="navbar navbar-expand-lg navbar-light ">
  <div class="container-fluid">
       <router-link to="/home" class="nav-brand nav-links" >Personal Fumes</router-link>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarNav">
      <ul class="navbar-nav">
        <nav class="navbar navbar-expand-lg navbar-light ">
  <div class="container-fluid">
       <router-link to="/home" class="nav-brand nav-links" >Personal Fumes</router-link>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse " id="navbarNav">
       <ul  class="navbar-nav w-100">
          <li><router-link to="/register" class="nav-link">Register</router-link></li>
          <li><router-link to="/login" class="nav-link">Log in</router-link></li>
          <li><router-link to="/admin" class="nav-link">Become an admin</router-link></li>
          <li><router-link to="/products" class="nav-link">Products</router-link></li>
          <li><router-link to="/cart" class="nav-link">Cart</router-link></li>
        </ul>
    </div>
  </div>
</nav>
      </ul>
    </div>
  </div>
</nav>
    </header>
</template>

<script>
export default {
    data(){
        return{
            logo:"https://i.postimg.cc/DfBt2NmB/logo-removebg-preview.png",
            scrollPosition:null,
            mobile:false,
            mobileNav:false,
            windowWidth:null,
        }
    },
    methods: {
     created(){
    window.addEventListener('resize',this.ScreenChecker);
    this.ScreenChecker()
  },
  methods:{
    toggleMobileNav(){
      this.mobileNav = !this.mobileNav
    },
     ScreenChecker(){
      this.windowWidth = window.innerWidth
      if(this.windowWidth <= 750){
        return this.mobile = true;
       
      }else{
       return this.mobile = false,
        this.mobileNav  = false;
        
      }
    }
  }  
    },
}
</script>
<style scoped>
   
   nav{
    background: #6D5E7D;
    opacity: 0.9;
    box-shadow: 20px ;
    position: fixed;
    top: 0;
    right: 0;
    left: 0;
    z-index:3;
    padding: 10px;
    width: 100%;
   }
   .nav-link{
    text-decoration:none;
    display:flex;
    align-items: center;
    
   }
   .nav-links:not(.nav-brand){
    display:flex;
    justify-content: end;
    
   }
   ul{
    list-style: none;
    display: flex;
    justify-content: flex-end;
     
   }
   li{
    text-align: end!important;
    font-size:bold;
    color:#000;
   }
   
   .link{
    text-decoration: none;
    color:#D8BFD8;
    border-bottom: none;
    padding: 5px;
   }
   .branding{
    width:30px;
    height:30px;
    margin-bottom:-15px;
   }
   .brand .nav-brand{
    height:100%;
    width:100%;
   }

   .nav-links .router-link-exact-active {
    border-bottom: display;
    transition: all 0.35s ease-in-out;
   }
   .icon{
    display: flex;
    justify-content: end;
   }
   .fa-bars{
    font-size: 200%;
   }
   .nav-link{
    text-decoration: none;
    color:#D8BFD8;
    border-bottom: none;
    padding: 5px;
   }
   .dropdown{
    display:flex;
    flex-direction: column;
    justify-content: end;
   }


</style>