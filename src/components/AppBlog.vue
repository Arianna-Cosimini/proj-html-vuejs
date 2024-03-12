<script>



export default {

    name: 'AppBlog',



    data() {
        return {
            articles: [
                {
                    image: "../../public/img/post1-1-570x450.jpg",
                    date: "December 16, 2020",
                    title: "Is Greece a Good Choice for Yacht Sailing?"
                },
                {
                    image: "../../public/img/post2-1-570x450.jpg",
                    date: "December 16, 2020",
                    title: "Seattle Yachts and Northwest Yachts Announce Merger"
                },
                {
                    image: "../../public/img/post3-1-570x450.jpg",
                    date: "December 16, 2020",
                    title: "Video: Superyacht 'Project Jupiter'Launched By Lurssen"
                },

            ]
        }
    },


    methods: {

    },






}

</script>

<template>

    <div id="article">
        <div id="content-article" class="text-center">
            <h3>Yachtsmen's Blog

            </h3>

            <div class="score">
                <div class="score-text"></div>
            </div>


            <div id="cards-item-article" class="d-flex flex-wrap ">
                <div v-for="currentArticle in articles" class="card-item px-4">
                    <div class="img-article">
                        <img :src="currentArticle.image" alt="">
                    </div>

                    <div class="text-card text-center">
                        <span>{{ currentArticle.date }}</span>
                        <h2>{{ currentArticle.title }}</h2>
                    </div>
                </div>
            </div>

            <button class="btn btn-outline-light">View All Blog Posts</button>

        </div>

    </div>



</template>

<style lang="scss">
@use '../styles/mixins' as *;
@use '../styles/variables' as *;

#article {


    background-color: #fff;

    #content-article {
        @include styleContainer;

        padding: 115px 0;

        h3 {
            font-size: 35px;
            font-weight: 700;
        }

        h2 {
            font-size: 16px;
        }

        span {
            font-size: 10px;
            color: #a8a8a8;
        }


        button {
            background-color: $PrimaryColor;
            padding: 10px 15px;
        }
    }

}


.score {
    background-color: #c1d3df;
    border-radius: 15px;
    height: 1px;

    position: relative;

    margin: 60px 0;

    .score-text {
        position: absolute;
        top: 0;
        left: 50%;

        width: 100px;
        height: 1px;

        border-radius: 15px;
        background-color: $PrimaryColor;
    }
}



.card-item {
    width: calc(100% / 3);
    margin-bottom: 50px;

}

.text-card {
    padding: 0 20px;
}
</style>