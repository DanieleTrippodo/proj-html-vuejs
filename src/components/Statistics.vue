<script>

export default{
  name:'Statistics',
  data() {
    return {
      
    }
  },
}
</script>

<template>
<article class="statitics-container">
  <div>
    <p>G</p>
    <p>G</p>
    <p>G</p>

</div>
  <div>
    <p>G</p>
    <p>G</p>
    <p>G</p>
  </div>
  <div>
   <p>G</p>
    <p>G</p>
    <p>G</p>
</div>
  <div>
    <p>G</p>
    <p>G</p>
    <p>G</p>
  </div>
</article>
</template>
<style>
 .statitics-container{
   display: flex;
   flex-direction: row;
   background-color: rgb(90, 40, 40);
   padding: 2rem;
   justify-content: center;

 }

 .statitics-container div{
    display: flex;
    flex-direction: column;
    color: white;
    height: 10rem;
    width: 10rem;
    font-size: 2rem;
   
    margin: 1rem 0rem 0 12rem;
    
    
}

</style>