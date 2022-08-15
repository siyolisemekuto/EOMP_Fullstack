<template>
<<<<<<< HEAD
    <nav class="navbar navbar-expand-lg">
  <div class="container-fluid">
    <router-link class="navbar-brand" :to="{name:'home'}">
    <span class="style">Personal Fumes</span>
    </router-link>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNavAltMarkup" aria-controls="navbarNavAltMarkup" aria-expanded="false" aria-label="Toggle navigation">
      <i class="fa-solid fa-bars"></i>
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
=======
  <div id="navbar">
      <nav class="navbar navbar-expand-md navbar-dark shadow p-3">
          <router-link to=/ class="navbar-brand active">Personal Fumes</router-link>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#nav-links" aria-controls="navbarNavAltMarkup" aria-expanded="false" aria-label="Toggle navigation">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div v-if="!user">
                <ul class="navbar-nav collapse navbar-collapse justify-content-end" id="nav-links">
                  <li><router-link to=/catalogue class=nav-link id="nav-about">Catalogue</router-link></li>
                  <li><router-link to=/cart class=nav-link id="nav-experience">Cart</router-link></li>                        
                  <li><router-link to=/profile class=nav-link id="nav-projects">Profile</router-link></li>
                  <!-- <li><router-link to=/contact class=nav-link  id="nav-contact">Contact</router-link></li> -->
                </ul>
            </div>
            <!-- <div v-else>
                 <li><router-link to=/register class=nav-link id="nav-testimonials">Register</router-link></li>
            </div> -->
        </nav>
>>>>>>> 716d115c232bcb6a7422f4c12b6d3fc6dd2520bc
      </div>
</template>

<script>
export default {
<<<<<<< HEAD
=======
  computed:{
    user() {
      return this.$store.state.user
    }
  },
>>>>>>> 716d115c232bcb6a7422f4c12b6d3fc6dd2520bc
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
    },
    mounted(){
      // this.$store.dispatch('fe')
    }
  }  
    }
</script>
<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Italianno&display=swap');

#navbar .navbar{
    background:#141414;
    opacity:0.9;
    box-shadow: 20px;
    position: fixed;
    top: 0;
    right: 0;
    left: 0;
<<<<<<< HEAD
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
=======
    z-index: 3;
}
.navbar-brand{
>>>>>>> 716d115c232bcb6a7422f4c12b6d3fc6dd2520bc
    font-family: 'Italianno', cursive;
    font-size:45px;
    font-weight:lighter;
    margin-left: 50px;
}
/* #nav-about{
    padding-right: 15px;
    text-decoration: none;
<<<<<<< HEAD
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
   .navbar-nav{
    display:flex;
    flex-wrap:no-wrap;
   }
   .fa-bars{
    font-size: 200%;
    color:white;
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
=======
    color: rgb(204, 214, 246);
    font-size: 15px;
} */
/* #nav-about:hover{
    color: rgb(255, 20, 147); 
}
#nav-experience{
    padding-right: 15px;
    text-decoration: none;
    color: rgb(204, 214, 246);
    font-size: 15px;
}
#nav-experience:hover{
    color: rgb(255, 20, 147); 
}
#nav-projects{
    padding-right: 15px;
    text-decoration: none;
    color: rgb(204, 214, 246);
    font-size: 15px;
}
#nav-projects:hover{
    color: rgb(255, 20, 147); 
}
#nav-testimonials{
    padding-right: 15px;
    text-decoration: none;
    color: rgb(204, 214, 246);
    font-size: 15px;
}
#nav-testimonials:hover{
    color: rgb(255, 20, 147); 
}
#nav-contact{
    padding-right: 15px;
    text-decoration: none;
    color: rgb(204, 214, 246);
    font-size: 15px;
}
#nav-contact:hover{
    color: rgb(255, 20, 147); 
} */
#navbar span{
    color: rgb(255, 20, 147);
    font-size: 15px;
}
nav ul li a {
    position: relative;
>>>>>>> 716d115c232bcb6a7422f4c12b6d3fc6dd2520bc

}

nav ul li a::after {
    content: '';
    width: 0;
    height: 3px;
    background: #C7A17F;
    position: absolute;
    left: 0;
    bottom: -6px;
    transition: 0.5s;
}

nav ul li a:hover::after{
    width: 100%;
}
.router-link-active{
  color:#C7A17F;
}

</style>