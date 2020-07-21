<template>
  <div id="app">
    <div class="box">
       <table-page :heder="heder" :result="result"></table-page>
               <table-page :heder="names" :result="result"></table-page>
<h1>toa e <span style="color:red;border: 1px solid black;font-style:italic"> hello </span> world </h1>
    </div> 
  </div>
</template>
<script>
//import Cards from "@/components/Cards.vue";
//import Login from "@/components/Login.vue";
//import Slider from "@/components/Slider.vue"; 
import TablePage from "@/components/TablePage.vue";
//import TableTwo from "@/components/TableTwo.vue"



export default {
  name: "App",

  components: {
  //  Cards,
   // Login
  //  Slider,
    TablePage,
    //TableTwo
    //Imag
  },
  data() {
    return {
      names:[
                {
                    name:"NAME"
                    
                },
                 {
                    name:"STREET"
                    
                },
                 {
                    name:"Mobile"
                    
                }
      ],
      heder:[
                {
                    name:"LAST"
                    
                },
                 {
                    name:"LASTNAME"
                    
                },
                 {
                    name:"Mobile"
                    
                }
            ],
            result:[
                {
                    name:"Simona",
                    lastname:"Kalajdziska",
                    mobile:"12345"
                },
                {
                    name:"Simona",
                    lastname:"Kalajdziska",
                    mobile:"12345"
                },
                {
                    name:"Simona",
                    lastname:"Kalajdziska",
                    mobile:"12345"
                },
                {
                    name:"Simona",
                    lastname:"Kalajdziska",
                    mobile:"12345"
                }

            ],
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
