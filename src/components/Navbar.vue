<template>
    <nav class="navbar">
  <div class="container">
    <h4>Personal Fumes</h4>
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
   h4{
    color:white;
    text-decoration: underline;
    font-size: 25px;
   }
   /* .nav-link{
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
   } */


</style>