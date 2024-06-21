<script>

export default{
    data() {
        return{
            sliderElements:[
                {
                    img: "hip_hop_wired_to_dance_make.jpg",
                    title: "Hip Hop Wired to Dance Make",
                    date: "06 November  2021",
                    text: "Driving Short Distances Music is a Music Genre That Includes Traditional Folk Music and The Contemporary Genre That Evolved From The Former",
                },
                {
                    img: "music_business-worldwide.jpg",
                    title: "Music Business Worldwide",
                    date: "27 May 2022",
                    text: "Accelerate Work and Drive Productivity The Beatles' Experimentation and Creative Freedom Led Other Bands to Experiment in Various Ways as Well.",
                },
                {
                    img: "giveaways_rock.jpg",
                    title: "Giveaways Rock to All",
                    date: "07 May 2022",
                    text: "Signs Your Car Battery Has To Be Replaced When The Dashboard Lights Start Flashing, This is a Sign the Battery is Dying. Several Issues Arise and",
                },
                {
                    img: "drowned_in_sound_feel_joy.jpg",
                    title: "Drowned in Sound Fell Joy",
                    date: "10 April 2022",
                    text: "Different Types of Music Content For Most Music Creators, They Take Their Work Very Seriously Because of The Emotional Attachment They May Harbor",
                },
                {
                    img: "dancing_astronaut_bounce_ipsum.jpg",
                    title: "Dancing Astrounat Bounce Ipsum",
                    date: "01 March 2022",
                    text: "Music Promotion Channels There are Really a Lot of Music Promotion Channels Out There. Being a Music Promotion Channel Involves a Lot of Work and",
                },
                {
                    img: "consequence_of_sound_make_us.jpg",
                    title: "Consequence of Sound Make Us",
                    date: "14 February 2022",
                    text: "Electronic Dance Music Rhythm and Blues Before This, R & B Was Known as 'Race Music,' a Term That Originated in The African American",
                },
                {
                    img: "artist_development_and_production.jpg",
                    title: "Artist Development and Production",
                    date: "07 December 2021",
                    text: "Characterised by Its Own Beat Patterns, the Lyrics Feature What is Often Extreme Violence and Talk of Criminal Acts. As a Result, There's Been",
                },
            ],
            indexScroll: 0,
        }
        
    },
    methods:{
        scrollLeft() {
            this.indexScroll--;
            if (this.indexScroll >= 0){
                this.$refs.scrollable.scrollBy({ left: -478, behavior: 'smooth' });
                console.log(this.indexScroll)
            } else{
                this.$refs.scrollable.scrollBy({ left: 2000, behavior: 'smooth' });
                this.indexScroll = this.sliderElements.length -2
                console.log(this.indexScroll)
            }
        },

        scrollRight() {
            this.indexScroll++;
            if(this.indexScroll < this.sliderElements.length -2){
                this.$refs.scrollable.scrollBy({ left: 478, behavior: 'smooth' });
                
                console.log(this.indexScroll)
            }
            else{
                this.$refs.scrollable.scrollBy({ left: -2000, behavior: 'smooth' });
                this.indexScroll = 0;
                console.log(this.indexScroll)
            }
        }
    },
}
</script>

<template>
<section>
    <div class="title">
        <p>music blog</p>
        <h2>best music blog</h2>
    </div>
    <button class="left"><img src="../assets/img/left-arrow.svg" alt="" @click="scrollLeft()"></button>
    <button class="right"><img src="../assets/img/right-arrow.svg" alt="" @click="scrollRight()"></button>
    <div class="slider" ref="scrollable">
        <article v-for="(element, index) in sliderElements">
            <div class="cover">
                <img :src="'../src/assets/img/' + element.img" alt="">
            </div>
            <div class="info">
                <h3>{{ element.title }}</h3>
                <h4><img src="../assets/img/date.svg" alt="">{{ element.date }}</h4>
                <p>{{ element.text }}</p>
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
                    margin-bottom: 1rem;
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