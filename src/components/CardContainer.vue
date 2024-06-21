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
    align-items: center;
    margin-left: 10rem;
   
  }

  .card-title{
    display: flex;
    margin-top: 1.5rem;
    flex-direction: column;
    
    align-items: center;
  
    
  
    h3{
    font-size: 3.7rem;
  }
   p{
    color: orange;
    font-size: 1.5rem;
    
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