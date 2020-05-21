<template>
  <div class="container">
    <div class="slider">
      <div class="slide">
        <img class="img" :src="getCurrentImage.src" :alt="getCurrentImage.text" />
      </div>
    </div>
    <button @click="nextSlide" :disable="currentSlide===images.length - 1">Next Slider</button>
    <button @click="prevSlide" :disable="currentSlide===0">Prev Slider</button>
  </div>
</template>
<script>
export default {
    data() {
        return{
            currentSlide : 0,
            images:[
                {
                src:'https://cdn.pixabay.com/photo/2015/12/12/15/24/amsterdam-1089646_1280.jpg',
                text : 'nature-summer-purple'
             },
             {
                 src: 'https://cdn.pixabay.com/photo/2016/02/17/23/03/usa-1206240_1280.jpg',
                 text : 'white-and-yellow-flower-with-green-stems'
             },
             {
                 src: 'https://cdn.pixabay.com/photo/2015/05/15/14/27/eiffel-tower-768501_1280.jpg',
                 text : 'flor-flower-garden'

             },
            ]
        }
    },
    computed:{
    getCurrentImage(){
    return this.images[this.currentSlide]
}
},
methods: {
    nextSlide(){
        let max = this.images.length - 1
        let current = this.currentSlide
        if(current != max) this.currentSlide++
    },
    prevSlide(){
        let min = 0
        let current = this.currentSlide
        if(current >= min) this.currentSlide--
    }
}

}
</script>
<style>
.img {
    width: 200px;
}

</style>