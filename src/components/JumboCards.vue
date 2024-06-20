<script>

export default{
    data() {
        return{
            jumboCards: [
                {
                    img: "image (10).svg",
                    title: "original ideas",
                    description: "Contrary Popular Belief, Lorem Ipsum Not Simply Ipsum Random Text.",
                },
                {
                    img: "image (11).svg",
                    title: "music studio",
                    description: "Contrary Popular Belief, Lorem Ipsum Not Simply Ipsum Random Text.",
                },
                {
                    img: "image (12).svg",
                    title: "acoustic covers",
                    description: "Contrary Popular Belief, Lorem Ipsum Not Simply Ipsum Random Text.",
                },
            ],
        }
    }
}
</script>

<template>
    <section>
        <article v-for="(card, index) in jumboCards">
            <div>
                <div>
                    <img :src=" '../src/assets/img/' + card.img " alt="">
                </div>
                <h2>{{ card.title }}</h2>
                <p>{{ card.description }}</p>
            </div>
        </article>
    </section>
</template>

<style lang="scss" scoped>

    section{
        display: flex;
        max-width: 1400px;
        margin: auto;

        article{
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            background-color: #121212;
            color: white;
            width: calc(100% / 3);
            height: 23rem;
            margin: 1rem;
            padding: 5rem 4.5rem;

            img{
                width: 106px;
                height: 106px;
                filter: invert(100%);
                margin-bottom: 1.5rem;
            }

            h2{
                text-transform: uppercase;
                margin-bottom: 1rem;
            }

            p{
                color: #b6b6b6;
            }
            div{
                text-align: center;
            }
        }
    }

</style>