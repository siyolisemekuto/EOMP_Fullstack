<template>
 <div>
  <h1>Personal Fumes</h1>
  <div class="container">
    <h1>Log in to your account.</h1>
    <form @submit.prevent="SubmitForm">
      <div >
        <input type="email" name="email" id="email" class="form-control" placeholder="Email" required  v-model="email">
        <input type="password" name="password" id="password" class="form-control" placeholder="Password" required v-model="Password">
      </div>
      <button type="submit" class="btn" v-on:click="Login()">Log in</button>
    </form>
    <router-link :to="{name:'register'}">Create and account</router-link>
  </div>
</div>    
</template>

<script>
export default {
  name: 'Login',
  methods: "POST"
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.page{
  display:block;
  padding:0 40px;
  background-color:rgb(250, 249, 246);
}
.container{
  background-color:white;
  width: 50vw;
  height: 68vh;
  margin-top: 150px;
  margin-bottom: 20px;
  border:1px solid;
  
}
h1{
  font-size:25px;
}
input{
    height: 48px;
    padding: 19px 16px 7px;
    /* margin: 20px;
    border: none; */
    border: 1px solid;
    /* background:inherit; */
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
 /* @media only screen and (max-width: 600px){ 
   p.about-text{
    width:75vw;
  }
  h1{
    margin-top:auto;
    display: flex;
    justify-content: center;
  }
}   */
</style>
