<script>
</script>

<template>
<article class="statitics-container icon">
  <div>
    <p><i class="fa-solid fa-child-reaching icon"></i></p>
    <p>900</p>
    <h6>CONCERTS</h6>

</div>
  <div>
    <i class="fa-solid fa-rocket icon"></i>
    <p>800</p>
    <h6>HAPPY CLIENTS</h6>
  </div>
  <div>
   <p><i class="fa-solid fa-trophy icon"></i></p>
    <p>400</p>
    <h6>MUSIC AWARDS</h6>
</div>
  <div>
    <p><i class="fa-solid fa-music icon"></i></p>
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
  
   padding: 4rem;
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
    font-size: 2rem;
     align-items: center;
    margin: 1rem 0rem 0 12rem;
    
    p{
      margin-bottom: 1rem;
    }



    .icon{
      font-size: 4rem;
      margin-bottom: 1rem;
      &:hover{
        color: orange;
      }
    }
}

}

</style>