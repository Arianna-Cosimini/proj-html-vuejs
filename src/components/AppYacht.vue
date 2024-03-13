<script>



export default {

    name: 'AppYacht',



    data() {
        return {
            yachts: [
                {
                    image: "../../public/img/services-1.jpg"
                },
                {
                    image: "../../public/img/services1.jpg"
                },
                {
                    image: "../../public/img/services2.jpg"
                },
                {
                    image: "../../public/img/services3.jpg"
                },
                {
                    image: "../../public/img/services4.jpg"
                },
                {
                    image: "../../public/img/services5.jpg"
                },
                {
                    image: "../../public/img/services6.jpg"
                },
                {
                    image: "../../public/img/services7.jpg"
                },
            ]
        }
    },


    methods: {

    },







}

</script>

<template>

    <div id="yachts">
        <div id="content-yachts" class="text-center">
            <h3>Our Yachts</h3>

            <div class="score">
                <div class="score-text"></div>
            </div>


            <div id="cards-yacht" class="d-flex flex-wrap ">
                <div v-for="yacht in yachts" class="yacht-item px-4">
                    <div id="img-card">
                        <img :src="yacht.image" alt="" class=" rounded">
                    </div>
                    <div id="hover">
                        <i class="fa-solid fa-anchor"></i>
                        <strong>Express</strong>
                    </div>
                </div>
            </div>

            <button class="btn btn-outline-light fw-semibold">View All</button>
        </div>
    </div>



</template>

<style lang="scss" scoped>
@use '../styles/mixins' as *;
@use '../styles/variables' as *;

#yachts {

    background-color: $PrimaryColor;

    #content-yachts {
        @include styleContainer;

        padding: 115px 0;

        h3 {

            color: white;
            font-size: 35px;
            font-weight: 700;
        }
    }
}


.score {
    background-color: $PrimaryColor;
    border-radius: 15px;
    height: 1px;

    position: relative;

    margin: 60px 0;

    .score-text {
        position: absolute;
        top: 0;
        left: 47%;

        width: 100px;
        height: 1px;

        border-radius: 15px;
        background-color: #c1d3df;
    }
}


.yacht-item {
    width: calc(100% / 4);
    margin-bottom: 80px;

    position: relative;

    #hover {
        display: none;
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);

        .fa-solid {
            color: $PrimaryColor;

            font-size: 50px;
            margin-bottom: 50px;
        }
    }

    &:hover {
        img {
            filter: grayscale(1.5);

        }

        #hover {
            display: block;
            display: flex;
            flex-direction: column;

            strong {
                text-transform: uppercase;
                color: white;
            }
        }
    }
}


button {
    @include styleButtonLight;

    &:hover {
        @include styleButtonLightHover;

    }
}


#cards-yacht {}
</style>