<script>
export default {
    data() {
        return {
            items: [
                { id: 1, text: 'HOME' },
                { id: 2, text: 'BLOG' },
                { id: 3, text: 'EVENTS', submenu: [
                    'CHORAL MUSIC',
                    'CONCERT BAND',
                    'OPERA CONCERTS',
                    'SYMPHONY ORCHESTRA',
                    'FAMILY CONCERTS'
                ] },
                { id: 4, text: 'GALLERY' },
                { id: 5, text: 'ABOUT US' },
                { id: 6, text: 'CONTACT US' },
                { id: 7, text: 'SHOP', submenu: [
                    'PRODUCT TYPE',
                    'SHOP PAGE'
                ] },
            ],
            selectedItem: null, 
            dropdownVisible: null,
        };
    },
    methods: {
        selectItem(id) {
            this.selectedItem = id; 
        },
        toggleDropdown(id) {
            this.dropdownVisible = id;
        },
        closeDropdown() {
            this.dropdownVisible = null;
        }
    },
};
</script>


<template>
    <div class="header-fixed" @click="closeDropdown">
        <div class="header-container" @click.stop>
            <div class="container-logo">
                <img src="../assets/img/Logo.png" alt="Logo">
            </div>
            <div class="container-li">
                <ul>
                    <li v-for="item in items" :key="item.id" 
                        :class="{ active: selectedItem === item.id }" 
                        @mouseover="toggleDropdown(item.id)">
                        <div @click="selectItem(item.id)">
                            {{ item.text }}
                            <i v-if="item.submenu" class="fa fa-caret-down"></i>
                        </div>
                        <ul v-if="item.submenu && dropdownVisible === item.id" 
                            class="dropdown">
                            <li class="dropdown-item" v-for="subitem in item.submenu" :key="subitem">{{ subitem }}</li>
                        </ul>
                    </li>
                    <li class="img-hover">
                        <img src="../assets/img/image (23).svg" alt="" class="img-search"> 
                    </li>
                </ul>
            </div>
        </div>
    </div>
    
</template>




<style lang="scss" scoped>

.container-logo img{
    padding-left: 1.6rem;
    width: 12rem;
}

.header-container {
    background-color: black;
    height: 100px;
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding-left: 1rem;
    padding-right: 1rem;
    box-shadow: 0px 4px 19px -5px rgba(255,255,255,0.17);
}
ul {
    display: flex;
    align-items: center;
    color: white;
    gap: 3rem;
    position: relative;
}
li {
    list-style: none;
    font-size: 15px;
    font-weight: 600;
    cursor: pointer;
    position: relative;
}
li:hover {
    color: #f2870c;
}
li.active {
    color: #f2870c;
}
.img-search {
    filter: brightness(0) invert(1);       
    height: 25px;
    padding-right: 2rem;
}
.header-fixed {
    position: fixed;
    top: 0;
    width: 100%;
    z-index: 3;
}
.img-hover:hover img {
    filter: brightness(0) saturate(100%) invert(54%) sepia(95%) saturate(1427%) hue-rotate(357deg) brightness(97%) contrast(95%);
}
.dropdown {
    position: absolute;
    top: 100%;
    left: 0;
    background-color: rgb(36, 35, 35);
    color: white;
    padding: 0.5rem 0; 
    display: block;
    min-width: 200px;
    z-index: 2; 
    margin-top: 2.2rem;
}
.dropdown-item {
    padding: 0.5rem 1rem;
    cursor: pointer;
    border-bottom: 1px solid rgb(67, 67, 67); 
    display: flex;
    align-items: center;
    height: 50px; 
}
.dropdown-item:last-child {
    border-bottom: none; 
}
.dropdown-item:hover {
    color: #f2870c; 
}
</style>