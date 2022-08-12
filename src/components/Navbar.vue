<template>
    <nav class="navbar navbar-expand-lg">
  <div class="container-fluid">
    <router-link class="navbar-brand" :to="{name:'home'}">
    <span class="style">Personal Fumes</span>
    </router-link>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNavAltMarkup" aria-controls="navbarNavAltMarkup" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarNavAltMarkup">
      <div class="navbar-nav">
        <div v-if="!user">
          <router-link class="nav-link" :to="{name:'catalogue'}">Catalogue</router-link>
          <router-link class="nav-link" :to="{name:'cart'}">Cart</router-link>
          <router-link class="nav-link" :to="{name:'profile'}">Profile</router-link>
        </div>
        <!-- <div v-else>
          <router-link class="nav-link" :to="{name:'register'}">Register</router-link>
        </div> -->
      </div>
    </div>
  </div>
</nav>
</template>

<script>
export default {
    data(){
        return{
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
@import url('https://fonts.googleapis.com/css2?family=Italianno&display=swap');
   nav{
    background-color: #141414;
    box-shadow: 10px ;
    position: fixed;
    top: 0;
    right: 0;
    left: 0;
    z-index:3;
    padding: 10px;
    width: 100%;
   }
   .navbar{
    display: flex;
    flex-wrap: nowrap;
    align-items: center;
    justify-content: space-between;
   }
   .navbar-brand{
    color:white;
    font-size: 25px;
    margin-top: 15px;
   }
   .container-fluid{
    height:50px;
   }
   span{
    font-family: 'Italianno', cursive;
    font-size:45px;
    font-weight:lighter;
    margin-left: 50px;
   }
 .nav-link{
    text-decoration:none;
   }
   
   ul{
    list-style: none;
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

   /* .nav-links .router-link-exact-active {
    border-bottom: display;
    transition: all 0.35s ease-in-out;
   } */
   /* .icon{
    display: flex;
    justify-content: end;
   } */
   .fa-bars{
    font-size: 200%;
   }
   .nav-link{
    text-decoration: none;
    color:#D8BFD8;
    border-bottom: none;
    padding: 5px;
   }
   /* .dropdown{
    display:flex;
    flex-direction: column;
    justify-content: end;
   }  */


</style>