<script>

import AppNavBar from './AppNavBar.vue'

export default {

    name: 'AppHeader',

    components: {
        AppNavBar,
    },


    data() {
        return {
            activeSlideIndex: 0,


            links: [
                {
                    link: "About",
                },
                {
                    link: "Services",
                },
                {
                    link: "yachts",
                },
                {
                    link: "reservations",
                },
                {
                    link: "blog",
                },
                {
                    link: "contacts",
                },
            ],

            slides: [
                {
                    image: '../../public/img/bg1-1.jpg',
                    title: "QuickWind",
                    text: "all kinds of boats, yacht charters and sailing destinations for hobbyist yachtsmen and women!",
                    button: "Learn More",
                },
                {
                    image: '../../public/img/bg2.jpg',
                    title: "QuickWind",
                    text: "all kinds of boats, yacht charters and sailing destinations for hobbyist yachtsmen and women!",
                    button: "Learn More",
                },
                {
                    image: '../../public/img/bg3.jpg',
                    title: "QuickWind",
                    text: "all kinds of boats, yacht charters and sailing destinations for hobbyist yachtsmen and women!",
                    button: "Learn More",
                },
            ]
        }
    },


    methods: {
        changeSlide(index) {
            console.log(index)
            this.activeSlideIndex = index
        },
    }





}

</script>

<template>

    <div class="carousel">
        <div class="slides" v-for="(currentImage, index) in slides" :key="index"
            :class="{ 'active': index === activeSlideIndex }">
            <AppNavBar :menuLinks="links"></AppNavBar>
            <img :src="currentImage.image" alt="">
            
                <div class="carousel-content">
                    <div class="hero-text w-50">
                        <h1 class="display-1 fw-bold">{{ currentImage.title }}</h1>
                        <p>{{ currentImage.text }}</p>
                        <button class="btn btn-outline-light fw-semibold">{{ currentImage.button }}</button>
                    </div>
                   

                </div>
           
        </div>
        <div class="score-carousel">
            <span v-for="(currentImage, index) in slides" :key="index" @click="changeSlide(index)"
                :class="{ 'active': index === activeSlideIndex }"></span>
        </div>
    </div>



</template>

<style lang="scss">
@use '../styles/mixins' as *;
@use '../styles/variables' as *;



.carousel {
    position: relative;
}

.slides {
    display: none;
}

.slides.active {
    display: block;
}

.score-carousel {
    position: absolute;
    bottom: 50px;
    left: 50%;
    transform: translateX(-50%);

    display: flex;
    gap: 50px;
}

.score-carousel span {
    display: inline-block;
    width: 10px;
    height: 10px;
    border-radius: 50%;
    background-color: white;
    margin: 0 5px;
    cursor: pointer;
}

.score-carousel span.active {
    background-color: $PrimaryColor;
    transform: scale(1.5)
}

.carousel-content{

    @include styleContainer;

    position: absolute;
    top: 40%;
    
    display: flex;
    justify-content: center;
    padding: 0 100px;
    color: white;
}
.hero-text {

    h1 {
        font-size: 94px;
    }

    p {
        font-size: 20px;
    }
}
</style>