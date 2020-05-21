<template>
    <div class="cards">
      <slot>
      <h1 class="title">{{ title }}</h1>
      <h2>{{ title5 }}</h2>
      <h3>{{ tekst5 }}</h3>
      <p v-if="show">{{ tekst }}</p>
      <p v-else>{{ tekst2 }}</p>
      <button @click="send" class="btn">go</button>
      </slot>
  </div>
</template>

<script>
export default {
  
    data (){
        return {
            show:true,
            selectedFile: null
        }
    },
    name:"Cards",
    props:{
      title:{
        type:String
      },
      tekst:{
        type:String
      },
      tekst2:{
          type:String
      },
      title5:{
        type:String
      },
      tekst5:{
        type:String
      }
      
    
    },
    
    methods:{
        send() {
            this.show = !this.show;
        },
        
    }
    

}
</script>

<style>
.cards {
  width: 500px;
  height: 350px;
  background: gray;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: center;
  border-right: 2px solid white;
}
.btn {
  width: 200px;
  height: 50px;
  background: green;
  color: white;
  border: none;
  cursor: pointer;
}
.btn:hover {
  opacity: 0.7;
}

</style>
