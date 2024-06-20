<script>
   export default {
    data() {
        return {
            items: [
                { id: 1, text: 'HOME' },
                { id: 2, text: 'BLOG' },
                { id: 3, text: 'EVENTS' },
                { id: 4, text: 'GALLERY' },
                { id: 5, text: 'ABOUT US' },
                { id: 6, text: 'CONTACT US' },
                { id: 7, text: 'SHOP' },
            ],
            selectedItem: null, 
        };
    },
    methods: {
        selectItem(id) {
            this.selectedItem = id; 
        },
    },
};
</script>

<template>
    <div class="header-fixed">
        <div class="header-container">
    <div class="container-logo">
        <img src="../assets/img/Logo.png" alt="Logo">
    </div>
    <div class="container-li">
        <ul>
            <li v-for="item in items" :key="item.id" :class="{ active: selectedItem === item.id }" @click="selectItem(item.id)">
                {{ item.text }}
            </li>
            <li class="img-hover">
                <img src="../assets/img/image (23).svg" alt="" class="img-search"> 
            </li>
        </ul>
    </div>
  </div>
    </div>
  
</template>

<style scoped>
    .header-container{
        background-color: black;
        height: 100px;
        width: 100%;
        display: flex;
        align-items: center;
        justify-content: space-between;
        padding-left: 1rem;
        padding-right: 1rem;
    }
    ul{
        display: flex;
        align-items: center;
        color: white;
        gap: 3rem;
    }
    li{
        list-style: none;
        font-size: 20px;
        font-weight:550;
        cursor: pointer;
    }
    li:hover{
        color: orange;
    }
    li.active {
    color: orange;
    }
    .img-search{
        filter: brightness(0) invert(1);
        height: 25px;
        padding-right: 2rem;
    }
    .header-fixed{
        position: fixed;
        top: 0;
        bottom: 50px;
        width: 100%;
        z-index: 3;
    }
    .img-hover:hover img{
        filter: invert(55%) sepia(100%) saturate(1000%) hue-rotate(-20deg);
    }
    

</style>