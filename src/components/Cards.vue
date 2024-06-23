<script>


export default{
data() {
    return {
        CardImage: [
              {
              image:"gallery1.jpg",
              title:'man singing',
              description:'A ROLL AND BANG THE FLOOR'
              },
              {
               image:'gallery2.jpg',
               title:'microphone',
              description:'YOUR MELODY TO OUR MUSIC'

              },
              {
                image:'gallery3.jpg',
                title:'drums',
              description:'TOUCHING HEAVEN FREQUENCY'
              },
              {
                image:'gallery4.jpg',
                title:'man playng guitar back',
             description:'MUSIC MAKES STRONGE BEATS'
              },
              {
                image:'gallery5.jpg',
                title:'man playng guitar front',
                description:'SOUND IS THE SPARK OF TIME'
              },
              {
                image:'gallery6.jpg',
                title:'guitar image',
                description:'MAKE YOUR NIGHT GROOVY'
              }


        ]
    }
},

}

</script>



<template>

  <div class="card" v-for="(card, index) in CardImage" :key="index">
    <div class="image">
    <img :src=" '../src/assets/img/' + card.image"  :alt="card.title"> 
  </div>
    <span><h3> {{ card.description }}</h3>
      <p> Stream On : <i class="fa-brands fa-spotify  icon"></i> <i class="fa-brands fa-youtube  icon"></i> <i class="fa-solid fa-music icon"></i> <i class="fa-brands fa-soundcloud icon"></i>   <i class="fa-brands fa-safari  icon"></i> </p>
    </span> 
  </div>

</template>
<style scoped>
.card{
    width: 30rem ;
    height: 32rem;
    display: flex;
    margin: 1rem;
    display: flex;
    flex-direction: column;
    align-items: center;
  

  span{

      margin: 0.5rem 0 0;
      padding-bottom: 1rem;

      h3{
      font-size: 1.7rem;
      }

      p{
      color: #d8d8d8;
      margin-left: 1.5rem;
      font-family: "open-sans", sans-serif;
      }
  }

  .image{

  overflow: hidden;

    img{
        width: 30rem;
        height: 30rem;
        
      transition: transform .2s;
        &:hover{
          transform: scale(1.1);
        }
    }
  }
}

.icon{
  margin-left:1rem;
  color: #ffffff;
  font-size: 1rem;
  
  &:hover{
  color:orange;
  }
}
</style>