<script>
   export default {
    data() {
        return {
           
        };
    },
    
};
</script>

<template>
  <div class="group-image">
    <img src="../assets/img/instagram_img1.jpg" alt="">
    <img src="../assets/img/instagram_img2.jpg" alt="">
    <img src="../assets/img/instagram_img3.jpg" alt="">
    <img src="../assets/img/instagram_img4.jpg" alt="">
    <img src="../assets/img/instagram_img5.jpg" alt="">
    <img src="../assets/img/instagram_img6.jpg" alt="">
    <img src="../assets/img/instagram_img7.jpg" alt="">
    <img src="../assets/img/instagram_img8.jpg" alt="">
  </div>
  
</template>

<style scoped>
.group-image{
    display: flex;
    overflow: hidden;
    
}
.group-image>img:hover{
    transform: scale(1.1);
}
img{
    width: calc(100% / 8);
}    
</style>