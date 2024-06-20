<script>
import Cards from '../components/Cards.vue'
export default{
    name:'CardContainer',

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

<style lang="scss" scoped>
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
    margin-left: 59rem;
  }

  .card-title p{
    color: orange;
  }
  .main-card-container{
    background-color: black;
    color: white;
    display: flex;
     flex-direction: column;
    justify-content: center;
  }
</style>