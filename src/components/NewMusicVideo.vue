<script>
export default {
    methods: {
        openLink() {
            window.open('https://www.youtube.com/watch?v=lTZLlzLJ68o&t=', '_blank');
        }
    }
};
</script>

<template>

        <div class="container-music-video" @click="openLink">
            <div class="container-content-music-video">
                <div class="container-play">
                    <i class="icon-container">
                        &#9654; 
                    </i>
                </div>

                <p>
                    NEW MUSIC VIDEO
                </p>
            </div>
            
        </div>
    

</template>

<style scoped>
    .container-music-video{
        display: flex;
        align-items: center;
        justify-content: center;
        background-image: url(../assets/img/Video-1024x361.jpg);
        background-repeat: no-repeat;
        background-size: cover;
        height: 680px;
        
    }
    .container-content-music-video{
        display: flex;
        align-items: center;
        justify-content: center;
        flex-direction: column;
        color: white;
    }
    p{
        margin-top: 1.5rem;
        font-size: 65px;
        font-weight: 700;
    }
    img{
        height: 50px;
        width: auto;
    }
    .container-play{
        display: flex;
        align-items: center;
        justify-content: center;
        border-radius: 50%;
        height: 90px;
        width: 90px;
        border: 4px solid;
        color: #f2870cd7;
        cursor: pointer;
        &:hover {
            color: #f2870c;
        }
    }
    i{
        font-size: 25px;
        font-style: normal;
        padding-left: .3rem;
    }

</style>