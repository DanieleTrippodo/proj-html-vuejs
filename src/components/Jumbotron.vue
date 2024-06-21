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
    }
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
      <span class="arrow left" @click="prevSlide">&#9664;</span>
      <span class="arrow right" @click="nextSlide">&#9654;</span>
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
}
.content {
  z-index: 2;
}
h1 {
  color: orange;
  margin-bottom: 0;
  font-size: 2em;
  text-transform: uppercase;
  font-weight: bold;
}
p {
  color: white;
  font-size: 7em;
  margin-bottom: 3rem;
  text-transform: uppercase;
  font-weight: bold;
}
ReadMore {
  padding: 1rem 3rem;
  background-color: none;
  border: 1px solid orange;
  color: white;
  font-size: 1.3em;
  cursor: pointer;
}

.arrows {
  position: absolute;
  top: 50%;
  width: 100%;
  display: flex;
  justify-content: space-between;
  transform: translateY(-50%);
}
.arrow {
  font-size: 1rem;
  color: white;
  cursor: pointer;
  user-select: none;

  padding-top: .8rem;
  padding-bottom: .8rem;
  padding-right: 1rem;
  padding-left: 1rem;
  background-color: rgba(0, 0, 0, 0.753);
}
.arrow.left {
  margin-left: 1rem;
}
.arrow.right {
  margin-right: 1rem;
}
</style>