<template>
  <div>

    <form>
  <div class="imgcontainer">
    <img src="img/man.png" alt="Avatar" class="avatar">
  </div>

  <div class="container">
    <label for="uname"><b>Username</b></label>
    <input type="text" placeholder="Enter Username" v-model="name" name="uname" required>

    <label for="uname"><b>Email</b></label>
    <input type="text" placeholder="Enter email" v-model="email" name="email" required>


    <label for="psw"><b>Password</b></label>
    <input type="password" placeholder="Enter Password"  v-model="password" name="psw" required>

    <button type="submit" @click.prevent="login()">Login</button>
  
  </div>

  <div class="container" style="background-color:#f1f1f1">
    <button type="button" class="cancelbtn">Cancel</button>
    <span class="psw">Forgot <a href="#">password?</a></span>
  </div>
</form>
   
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',

  data() {
    return {
      name:null,

      email:null,

      password:null,
    }


    },
    

    methods:{
      login(){

        console.log(this.name);
        console.log(this.email);
        console.log(this.password);


        this.$router.replace({name:'dashboard'});


      }


  },



}

</script>
  



<style>


form {
  border: 3px solid #f1f1f1;
  width: 300px;
  margin-left: 40%;
}

/* Full-width inputs */
input[type=text], input[type=password] {
  width: 100%;
  padding: 12px 20px;
  margin: 8px 0;
  display: inline-block;
  border: 1px solid #ccc;
  box-sizing: border-box;
}


button {
  background-color: #04AA6D;
  color: white;
  padding: 14px 20px;
  margin: 8px 0;
  border: none;
  cursor: pointer;
  width: 100%;
}

button:hover {
  opacity: 0.8;
}

.cancelbtn {
  width: auto;
  padding: 10px 18px;
  background-color: #f44336;
}


.imgcontainer {
  text-align: center;
  margin: 24px 0 12px 0;
}

/* Avatar image */
img.avatar {
  width: 40%;
  border-radius: 50%;
}

/* Add padding to containers */
.container {
  padding: 16px;
}

/* The "Forgot password" text */
span.psw {
  float: right;
  padding-top: 16px;
}

/* Change styles for span and cancel button on extra small screens */
@media screen and (max-width: 300px) {
  span.psw {
    display: block;
    float: none;
  }
  .cancelbtn {
    width: 100%;
  }
}

</style>


