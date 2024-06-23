<!-- Qui va la logica del componente (Vue3 + Javascript) -->
<script>
import ReadMore from './ReadMore.vue'

export default {
  name: 'Jumbotron',
  data() {
    return {
      currentSlide: 0,
      slides: [
        {
          image: './src/assets/img/sfondo1.png',
          title: 'Instrumental Rock',
          description: 'Music of the Spirit',
        },
        {
          image: './src/assets/img/sfondo2.png',
          title: 'Instrumental Rock',
          description: 'Music in this Video',
        },
      ]
    };
  },
  methods: {
    nextSlide() {
      this.currentSlide = (this.currentSlide + 1) % this.slides.length;
    },
    prevSlide() {
      this.currentSlide = (this.currentSlide - 1 + this.slides.length) % this.slides.length;
    },
    startSlider: function () {
      setInterval(() => {
        this.currentSlide = (this.currentSlide + 1) % this.slides.length;
      }, 5000); 
    }
  },
  mounted(){
    this.startSlider()
  }
};
</script>



<!-- Qui va il contenuto di questo elemento (HTML) -->
<template>
  <div :style="{ backgroundImage: `url(${slides[currentSlide].image})` }" class="jumbotron">
    <div class="content">
      <h1>{{ slides[currentSlide].title }}</h1>
      <p>{{ slides[currentSlide].description }}</p>

      <ReadMore> Read More </ReadMore>

    </div>

    <div class="arrows">
      <button class="arrow left" @click="prevSlide"> <img src="../assets/img/left-arrow.svg" alt=""></button>
      <button class="arrow right" @click="nextSlide"><img src="../assets/img/right-arrow.svg" alt=""></button>
    </div>
  </div>
</template>



<!-- Qui va lo stile CSS di questo elemento (CSS) -->
<style lang="scss" scoped>
.jumbotron {
  position: relative;
  width: 100%;
  height: 58rem;
  background-size: cover;
  background-position: center;
  color: white;
  display: flex;
  align-items: center;
  justify-content: center;
  text-align: center;
  transition: background-image 1s ease-in-out;
  margin-top: 4rem;
  margin-bottom: .4rem;
  padding-bottom: 11rem;

  &:hover .arrows{
    display: flex;
  }
}
.content {
  z-index: 2;
}
h1 {
  color: #f2870c;
  margin-bottom: 2rem;
  font-size: 1.5rem;
  text-transform: uppercase;
  font-weight: bold;
}
p {
  color: white;
  font-size: 6em;
  margin-bottom: 3rem;
  text-transform: uppercase;
  font-weight: bold;
}
ReadMore {
  padding: .7rem 3.5rem;
  background-color: none;
  border: 1px solid #f2870c;
  color: white;
  font-size: 1em;
  cursor: pointer;
  text-transform: uppercase;
}

.arrows {
  position: absolute;
  top: 50%;
  width: 100%;
  display: flex;
  justify-content: space-between;
  transform: translateY(-50%);
  display: none;
}
.arrow {
  font-size: 1rem;
  color: white;
  cursor: pointer;
  user-select: none;
  padding: .8rem 1rem;
  background-color: rgba(0, 0, 0, 0.397);
  border: none;
  margin: 1.5rem;
  cursor: pointer;
  img{
    width: .5rem;
  }

  &:hover{
    background-color: rgba(0, 0, 0, 0.651);
  }
}

</style>