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

    <div id="hero"  v-for="(currentImage, index) in slides" @click="changeSlide(index)">
        <img :src="currentImage.image" alt="">

        <AppNavBar :menuLinks="links"></AppNavBar>
        <div class="container">
            <div class="hero-text" >
                <h1 class="display-1 fw-bold">{{ currentImage.title }}</h1>
                <p>{{ currentImage.text }}</p>
                <button>{{ currentImage.button }}</button>
            </div>

        </div>
    </div>

</template>

<style lang="scss">
@use '../styles/mixins' as *;
@use '../styles/variables' as *;

#hero {
    position: relative;

    img {
        object-fit: cover;
    }
}

.container {
    @include styleContainer;

    .hero-text {
        position: absolute;
        top: 40%;

        padding: 0 100px;
        color: white;

        h1 {
            font-size: 94px;
        }

        p {
            font-size: 20px;
        }
    }

}
</style>