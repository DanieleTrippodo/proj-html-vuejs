<script>

export default{
    data() {
        return{
            sliderElements:[
                {
                    img: "hip_hop_wired_to_dance_make.jpg",
                    title: "Hip Hop Wired to Dance Make",
                    date: "06 November  2021",
                    text: "Driving short distances music is a music genre that includes traditional folk music and the contemporary genre that evolved from the former",
                },
                {
                    img: "music_business-worldwide.jpg",
                    title: "Music Business Worldwide",
                    date: "27 May 2022",
                    text: "Accelerate work and drive productivity The Beatles' experimentation and creative freedom led other bands to experiment in various ways as well.",
                },
                {
                    img: "giveaways_rock.jpg",
                    title: "Giveaways Rock to All",
                    date: "07 May 2022",
                    text: "Signs Your Car Battery Has To Be Replaced When the dashboard lights start flashing, this is a sign the battery is dying. Several issues arise and",
                },
                {
                    img: "drowned_in_sound_feel_joy.jpg",
                    title: "Drowned in Sound Fell Joy",
                    date: "10 April 2022",
                    text: "Different Types of Music Content For most music creators, they take their work very seriously because of the emotional attachment they may harbor",
                },
                {
                    img: "dancing_astronaut_bounce_ipsum.jpg",
                    title: "Dancing Astrounat Bounce Ipsum",
                    date: "01 March 2022",
                    text: "Music Promotion Channels There are really a lot of music promotion channels out there. Being a music promotion channel involves a lot of work and",
                },
                {
                    img: "consequence_of_sound_make_us.jpg",
                    title: "Consequence of Sound Make Us",
                    date: "14 February 2022",
                    text: "Electronic Dance Music Rhythm and Blues Before this, R & B was known as 'race music,' a term that originated in the African American",
                },
                {
                    img: "artist_development_and_production.jpg",
                    title: "Artist Development and Production",
                    date: "07 December 2021",
                    text: "Characterised by its own beat patterns, the lyrics feature what is often extreme violence snd talk of criminal acts. As a result, there's been",
                },
            ]
        }
    }
}
</script>

<template>
<section>
    <div class="title">
        <p>music blog</p>
        <h2>best music blog</h2>
    </div>
    <button class="left"><i class="fa-solid fa-chevron-left "></i></button>
    <button class="right"><i class="fa-solid fa-chevron-right "></i></button>
    <div class="slider">
        <article v-for="(element, index) in sliderElements">
            <div>
                <img :src="'../src/assets/img/' + element.img" alt="">
            </div>
            <div class="info">
                <h3>{{ element.title }}</h3>
                <h4>{{ element.date }}</h4>
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
    padding: 5rem 0;
    position: relative;

    button{
        position: absolute;
        top: 51%;
        padding: 1rem;
        font-size: 2rem;
        background-color: transparent;
        border: none;
        color: white;
    }

    button.left{
        left: -2.5rem;
    }

    button.right{
        right: -3.5rem;
    }

    div.title{

        p{
            color: #e37f0a;
            text-transform: uppercase;
            text-align: center;
            font-size: 1.2rem;
        }

        h2{
            color: white;
            text-transform: uppercase;
            text-align: center;
            font-size: 5rem;
        }
    }

    div.slider{
        display: flex;
        overflow: scroll;
        max-width: 1400px;
        scrollbar-width: none;
        article{
            min-width: calc(100% / 3);
            margin: 1rem;

            img{
                width: 100%;
            }

            div.info{
            
                h3{
                    color: white;
                    font-size: 2rem;
                }

                h4{
                    color: #e37f0a;
                    font-size: 1.2rem;
                }

                p{
                    color: #b6b6b6;
                    font-size: 1.2rem
                }
            }
        };
    };
}

</style>