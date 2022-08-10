<template>
  <div class="container">
    <h1>landing/login</h1>
    <form @submit.prevent="SubmitForm">
      <div >
        <input type="email" name="email" id="email" class="form-control" placeholder="Email" required  v-model="email">
        <input type="password" name="password" id="password" class="form-control" placeholder="Password" required v-model="Password">
      </div>
      <button type="submit" class="btn" v-on:click="Login()">Log in</button>
    </form>
    <router-link :to="{name:'register'}">Create and account</router-link>
  </div>
       
</template>

<script>
export default {
  name: 'Login',
  methods: {
    login(){
    if(this.input.email == "user.email" && this.input.password === "user.password"){
      console.log("logged in");
    } else{
      console.log("the email or password is incorrect")
    }
  }, 
}
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

.container{
  width: fit-content;
  height: fit-content;
  margin: auto;
  display: flex;
  flex-direction: column;
  padding: 10px;
}
.inputs{
    width: 70%;
    padding: 10px;
    margin: 20px;
    border: none;
    border-bottom: 1px solid;
    background:inherit;
}
:-ms-input-placeholder::after{
    display: none;
}
.btn{
    margin-top: 20px;
    padding: 5px;
    font-size: large;;
    border-radius: 9px;
}
form{
  width: fit-content;
  display: flex;
  flex-direction:column;
  justify-content: center;
}
 @media only screen and (max-width: 600px){ 
   p.about-text{
    width:75vw;
  }
  h1{
    margin-top:auto;
    display: flex;
    justify-content: center;
  }
}  
</style>
