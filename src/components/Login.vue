<template>
 <div class="col-md-6">
  <div class="container ">
    <h1>Log in to your account.</h1>
    <form @submit.prevent="SubmitForm">
      <div >
        <input type="email" name="email" id="email" class="form-control" placeholder="Email" required  v-model="email">
        <input type="password" name="password" id="password" class="form-control" placeholder="Password" required v-model="Password">
      </div>
      <button type="submit" class="btn" v-on:click="login()">Log in</button>
    </form>
    <router-link :to="{name:'register'}" class="register">Register an account</router-link>
  </div>
</div>    
</template>

<script>
export default {
  name: "Login",
  // users() {
  //   return {
  //     email: "",
  //     password: ""
  //   };
  // },
  methods: {
    async login() {
      let response = await this.$store.dispatch("fetchUser", {
        email: this.email,
        password: this.password
      })
      console.error(error);
      
},
 ...mapActions(["LogIn"]),
    async submit() {
      const User = new FormData();
      User.append("email", this.form.email);
      User.append("password", this.form.password);
      try {
        await this.LogIn(User);
        this.$router.push("/products");
        this.showError = false;
      } catch (error) {
        this.showError = true;
      }
    },
  }
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
  width: 40vw;
  height: 68vh;
  margin-top: 110px;
  margin-bottom: 20px;
  border:1px solid grayscale;
  box-shadow:0 5px 5px 0 rgba(0, 0, 0, 0.2);
  display:flex;
  flex-direction:column;
  align-items: center;
  justify-content: space-evenly;
}
h1{
  font-size:25px;
}
input{
    height: 48px;
    padding: 19px 16px 7px;
    width:300px;
    color:black;  
    margin-bottom:10px;

    /* margin: 20px;
    border: none; */
    border: 1px solid gray;
    /* background:inherit; */
}
button{
  background-color:#141414;
  color:white;
  border-radius: 0;
  height: 48px;
  padding: 19px 16px 7px;
  width:20rem;
  margin-top: 20px;
  padding: 5px;
  font-size: large;
}
button:hover{
  background-color:rgba(20,20,20,0.8);
  
}
.register{
  text-decoration:underline;
  color:#C7A17F;
}
:-ms-input-placeholder::after{
    display: none;
}

form{
  width: fit-content;
  display:flex;
  flex-direction:column;
  align-items: center;
  justify-content: space-evenly;
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
