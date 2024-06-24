<script>
    export default {
    data() {
        return {
            images: [
                {
                    img: 'instagram_img1.jpg',
                },
                {
                    img: "instagram_img2.jpg",
                },
                {
                    img: "instagram_img3.jpg",
                },
                {
                    img: "instagram_img4.jpg",
                },
                {
                    img: "instagram_img5.jpg",
                },
                {
                    img: "instagram_img6.jpg",
                },
                {
                    img: "instagram_img7.jpg",
                },
                {
                    img: "instagram_img8.jpg",
                },
                {
                    img: "instagram_img9.jpg",
                },
                {
                    img: "instagram_img10.jpg",
                }

            ]
        };
    },
    
};
</script>

<template>
    <section class="container">
        <div v-for="(image, index) in images" class="group-image">
            <img :src=" '../src/assets/img/' + image.img">
        </div>
    </section>
</template>

<style lang="scss" scoped>

section.container{
    display: flex;
    overflow-y: scroll;
    scrollbar-width: none;
    div.group-image{
        min-width: calc((100% / 8) - .1rem);
        aspect-ratio: 1/1;
        margin: .1rem;
        overflow: hidden;
        
        img{
            width: 100%;
            transition: transform .5s;
            object-fit: cover;
            cursor: pointer;
    
            &:hover{
                transform: scale(1.1);
            }
        }
    }
}
</style>