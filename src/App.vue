<template>
  <div id="app">
    <div class="box">
       
        <slider> </slider>
          <input type="text" name=" Firstname" v-model="input.firstname" placeholder="Firstname"/>
           <input type="text" name=" Lastname" v-model="input.lastname" placeholder="Lastname"/>
           <input type="text" name=" Phonenumber" v-model="input.phonenumber" placeholder="Phonenumber"/>
          <input type="text" name="username" v-model="input.username" placeholder="Username" />
        <input type="password" name="password" v-model="input.password" placeholder="Password" />
        <textarea v-model="input.textarea" rows="10" cols="20"> </textarea>
        <button type="button" @click="reset()">Reset</button>
    </div> 
  </div>
</template>
<script>
//import Cards from "@/components/Cards.vue";
//import Login from "@/components/Login.vue";
import Slider from "@/components/Slider.vue"; 


export default {
  name: "App",

  components: {
  //  Cards,
   // Login
    Slider,
    //Imag
  },
  data() {
    return {
      title2: "PRIVATNA GRADINKA",
      title1: "Salvador Aljende",
      tekst1: "Time",
      tekst2: "Lorem Ipsum is simply dummy text of the printing",
     title3: "email",
     tekst4: "password",
     input: {
                    username: "",
                    password: "",
                    firstname: "",
                    lastname: "",
                    phonenumber: "",
                    textarea: ""
                }
           
    };
  },
  methods:{
   reset() {
     if (this.input.username == "" && this.input.password == "" && this.input.firstname == "" && this.input.lastname == ""
   && this.input.phonenumber == "" && this.input.textarea == "" ) {
     alert("all fields are required")  
   } else {
     this.input.username = "";
this.input.password = "";
this.input.firstname = "";
this.input.lastname = "";
this.input.phonenumber = "";
this.input.textarea = "";
   }

   }
  }
};
</script>

<style>
.box {
  display: flex;
    width: 500px;
  height: 350px;
  -moz-background-clip: border-box;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items:stretch;
  padding: 10px;
  margin-top: 50px;
}
</style>
