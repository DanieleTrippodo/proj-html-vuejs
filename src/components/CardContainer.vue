<script>
import Cards from '../components/Cards.vue'
export default{


    components:{
        Cards
    },
    
    data() {
    return {
        
    }
}

}
</script>

<template>
<article class="main-card-container">
    <span class="card-title"><p>WHO WE ARE</p>
    <h3>SENSE THE JAZZ</h3>    </span>
    
    
    <div class="card-container">
    <Cards/>
    </div>




</article>


</template>

<style scoped>
  .card-container{
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    justify-content: center;
    align-items: center;
  }

  .card-title{
    display: flex;
    flex-direction: column;
    align-items: center;
  
    h3{
    font-size: 3.7rem;
  }
  p{
    color: #f2870c;
    font-size: 1rem;
    font-family: "opens-sans", sans-serif;
    font-weight: 600;
  }
}
  .main-card-container{
    background-color: black;
    color: white;
    display: flex;
    flex-direction: column;
    padding: 8rem;
  }
</style>