<script>
import JumboCards from './JumboCards.vue';
export default {
    name: 'WhoWeAre',
    data() {
        return {

        };
    },
    components:{
    JumboCards
    }
};
</script>

<template>
    <section class="container">
        <JumboCards/>
        <div class="sense-the-jazz">
            <section class="text-sense-the-jazz">
                <h3>WHO WE ARE</h3>
                <h1>SENSE THE JAZZ</h1>
                <p>The Story Of Jazz And Blues Society Is The Story Of Determination, Passion, Idealism, Community, And Of Course, <br>Music. Founded In 1985 And Incorporated In 1986, As A Community Based, Not-For-Profit, Charitable Arts <br>Organization Located In Vancouver, British Columbia, The Society, From The Very Beginning, Has Worked Diligently <br>To Establish Vancouver As A Centre For The Creation And Exchange Of Sounds And Ideas Between The Local, <br>National And International Music Communities.</p>
                <button type="submit">READ MORE</button>
            </section>
        </div>
    </section>
</template>

<style lang="scss" scoped>

section.container{
    position: relative;
}
.sense-the-jazz{
    background-color: black;
    padding: 19rem 0 8rem 0;
}
h3{
    
    color: #e37f0a;
    font-size: 1em;
    font-family: "opens-sans", sans-serif;
    font-weight: 600;
}
p{
    color: #b6b6b6;
    padding-top: 1rem;
    padding-bottom: 1rem;
    font-size: 1em;
    font-family: "open-sans", sans-serif;
    line-height: 2rem;
}
h1{
    font-size: 4em;
    color: white;
}
button{
    background-color: black;
    border: 1px solid #e37f0a;
    color:  white;
    width: 200px;
    height: 50px;
    font-weight: bold;
    margin-top: 1rem;
    cursor: pointer;
}
button:hover{
    background-color:#e37f0a;
    
}
.text-sense-the-jazz{
    display: flex;
    flex-direction: column;
    margin: 0 auto;
    align-items: center;
    text-align: center;
}
</style>