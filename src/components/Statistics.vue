<script>
</script>

<template>
<article class="statitics-container icon">
  <div>
    <img src="../assets/img/image (13).svg">
    <p>900</p>
    <h6>CONCERTS</h6>

</div>
  <div>
    <img src="../assets/img/image (14).svg">
    <p>800</p>
    <h6>HAPPY CLIENTS</h6>
  </div>
  <div>
    <img src="../assets/img/image (15).svg">
    <p>400</p>
    <h6>MUSIC AWARDS</h6>
</div>
  <div>
    <img src="../assets/img/image (16).svg">
    <p>1001</p>
    <h6>TOTAL SONG</h6>
  </div>
</article>
<div class="prova"></div>
</template>
<style scoped>
 .statitics-container{
   display: flex;
   flex-direction: row;
   background-color: rgb(90, 40, 40);
  
   padding: 10rem;
   justify-content: center;
   background-image: url(../assets/img/counter_parallax.jpg);
   background-attachment: fixed;
   
 h6{
  font-size:1.5rem;
 }



 div{
    display: flex;
    flex-direction: column;
    color: white;
    
    
    height: 10rem;
    width: 14rem;
    font-size: 3.5rem;
     align-items: center;
    margin: 1rem 0rem 0 12rem;
    
     img{
      width: 6rem;
      height: 6rem;
      filter: brightness(0) saturate(100%) invert(100%) sepia(100%) saturate(0%) hue-rotate(288deg) brightness(102%) contrast(102%);
       
      &:hover{
        filter: brightness(0) saturate(100%) invert(52%) sepia(99%) saturate(884%) hue-rotate(354deg) brightness(95%) contrast(99%);
      }

     }


    p{
      margin-bottom: 1rem;
    }



    
}

}

</style>