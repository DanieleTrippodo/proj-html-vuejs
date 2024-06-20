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
    width: 80%;
    margin-left: 20rem;
    
  }

  .card-title{
    display: flex;
    
    flex-direction: column;
    
    align-items: center;
  
  
  
    h3{
    font-size: 3rem;
  }
   p{
    color: orange;
  }
}
  .main-card-container{
    background-color: black;
    color: white;
    display: flex;
     flex-direction: column;
    justify-content: center;
    padding-bottom: 2rem;
  }
</style>