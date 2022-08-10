<template>
 <div class="container">
    <h1>Register</h1>
   <form @submit.prevent="SubmitForm">
          <div >
            <input type="text" name="full_name" id="full_name" class="inputs" placeholder="Full name" required v-model="Password">
            <input type="email" name="email" id="email" class="inputs" placeholder="Email" required  v-model="email">
            <input type="password" name="password" id="password" class="inputs" placeholder="Password" required v-model="Password">
            <input type="text" name="contact_number" id="contact_number" class="inputs" placeholder="Contact Number" required v-model="Password">
          </div>
          <button type="submit" class="btn">Register</button>
  </form>
  </div>
</template>

<script>
export default {
    name:'Register'
}
</script>

<style>
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