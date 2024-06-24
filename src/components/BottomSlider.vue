<script>
import { store } from '../store.js';
import axios from "axios";

export default{
    data() {
        return{
            store,
            indexScroll: 0,
        }
        
    },
    methods:{
        getTrending(){
            axios.get("http://152.89.170.170:3000/events/rock")
            .then((response) => {
                this.store.Events = response.data
                console.log(response.data)
            })
        },

        scrollLeft() {
            this.indexScroll--;
            if (this.indexScroll >= 0){
                this.$refs.scrollable.scrollBy({ left: -478, behavior: 'smooth' });
                console.log(this.indexScroll)
            } else{
                this.$refs.scrollable.scrollBy({ left: 3500, behavior: 'smooth' });
                this.indexScroll = this.store.Events.length -2
                console.log(this.indexScroll)
            }
        },

        scrollRight() {
            this.indexScroll++;
            if(this.indexScroll < this.store.Events.length -2){
                this.$refs.scrollable.scrollBy({ left: 478, behavior: 'smooth' });
                
                console.log(this.indexScroll)
            }
            else{
                this.$refs.scrollable.scrollBy({ left: -3500, behavior: 'smooth' });
                this.indexScroll = 0;
                console.log(this.indexScroll)
            }
        }
    },
    created(){
        this.getTrending()
    }
}
</script>

<template>
<section>
    <div class="title">
        <p>music events</p>
        <h2>incoming events</h2>
    </div>
    <button class="left"><img src="../assets/img/left-arrow.svg" alt="" @click="scrollLeft()"></button>
    <button class="right"><img src="../assets/img/right-arrow.svg" alt="" @click="scrollRight()"></button>
    <div class="slider" ref="scrollable">
        <article v-for="(event, index) in store.Events">
            <div class="cover">
                <img :src="event.image" alt="">
            </div>
            <div class="info">
                <h3>{{ event.event_name }}</h3>
                <p> <i class="fa-solid fa-location-dot"></i> {{ event.location }}</p>
                <h4><img src="../assets/img/date.svg" alt="">{{ event.start_date }}  / {{ event.end_date }}</h4>
                <p>{{ event.type }}</p>
            </div>
        </article>
    </div>
</section>
</template>

<style lang="scss" scoped>

section{
    display: flex;
    flex-direction: column;
    max-width: 1400px;
    margin: auto;
    padding: 7rem 0;
    position: relative;

    &:hover button{
        opacity: 1;
    }

    .cover {

        overflow: hidden;
        img{
            cursor: pointer;
            transition: transform .5s;
            height: 18rem;
            object-fit: cover;
            object-position: top;
            &:hover{
                transform: scale(1.1);
            }
        }
    }

    button{
        position: absolute;
        top: 51%;
        padding: 1rem;
        background-color: transparent;
        border: none;
        color: white;
        opacity: 0;
        cursor: pointer;
        transition: opacity .5s;

        img{
            width: 1rem;
        }
    }

    button.left{
        left: -3rem;
    }

    button.right{
        right: -3.5rem;
    }

    div.title{

        p{
            color: #e37f0a;
            text-transform: uppercase;
            text-align: center;
            font-size: 1rem;
            font-family: "Open-sans", sans-serif;
            font-weight: 600;
        }

        h2{
            color: white;
            text-transform: uppercase;
            text-align: center;
            font-size: 3.9rem;
            margin-bottom: 1rem;
        }
    }

    div.slider{
        display: flex;
        overflow: scroll;
        scrollbar-width: none;
        article{
            min-width: calc((100% / 3) - 1.7rem);
            margin: 1rem;

            img{
                width: 100%;
            }

            div.info{
            
                h3{
                    color: white;
                    font-size: 1.5rem;
                    text-transform: uppercase;
                    margin: 1rem 0;
                    cursor: pointer;
                    &:hover{
                        color: #e37f0a;
                    }
                }

                h4{
                    color: #e37f0a;
                    font-size: 1rem;
                    margin-bottom: .5rem;
                    margin-top: .5rem;
                    font-family: "Open-sans", sans-serif;
                    font-weight: 100;
                    img{
                        width: .9rem;
                        margin-right: .5rem;
                    }
                }

                p{
                    color: #b6b6b6;
                    font-size: 1rem;
                    font-family: "Open-sans", sans-serif;
                    font-weight: 100;
                    line-height: 1.8rem;
                }
            }
        };
    };
}

</style>