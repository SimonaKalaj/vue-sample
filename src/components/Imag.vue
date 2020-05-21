<template>
  <div class="imag" :style="{ 'background-image': 'url(' + backgroundImage + ')' }"></div>
</template>

<script>
export default {
  props:{
     backgroundImage:{
        type:String
      }
  }
}  
</script>
<style>
.imag {
  background-position: center;
  background-size: cover;
  width: 300px;
  height: 300px;
}
</style>
