<script>



export default {

    name: 'AppTestimonials',



    data() {
        return {

            activeSlideIndex: 0,

            testimonials: [
                {
                    image: "../../public/img/person0-p0a17bbqv6696rzdb2ly3jl0kdng6od3fj7vti5wi8.jpg",
                    text: "As a yact owner, after either of my regular maintenance checkups, i oftentimes find it necessary to do this or that kind of a repair. The thing is that i don't always have enough time (or sometimes the skill), to do all of the pairs all by myself.defineEmits.",
                    author: "-Albert Winning",
                },
                {
                    image: "../../public/img/person01-p0a17bbqv6696rzdb2ly3jl0kdng6od3fj7vti5wi8.jpg",
                    text: "As a yact owner, after either of my regular maintenance checkups, i oftentimes find it necessary to do this or that kind of a repair. The thing is that i don't always have enough time (or sometimes the skill), to do all of the pairs all by myself.defineEmits.",
                    author: "-Frank Sinatra",
                },
                {
                    image: "../../public/img/person03-p0a17bbqv6696rzdb2ly3jl0kdng6od3fj7vti5wi8.jpg",
                    text: "As a yact owner, after either of my regular maintenance checkups, i oftentimes find it necessary to do this or that kind of a repair. The thing is that i don't always have enough time (or sometimes the skill), to do all of the pairs all by myself.defineEmits.",
                    author: "-Marilyn Monroe",
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

    <div id="testimonials">
        <div id="content-testimonials" class="text-center">
            <h3>Testimonials</h3>

            <div class="score">
                <div class="score-text"></div>
            </div>

            <div class="testimonial-carousel">

                <div v-for="(currentTestimonial, index) in testimonials" id="feedback" :key="index"
                    :class="{ 'active': index === activeSlideIndex }"
                    class="text-start mx-5 pe-5">
                    <div class="img-testimonial">
                        <img :src="currentTestimonial.image" alt="">
                    </div>
    
                    <div class="text-testimonial">
                        <p>{{ currentTestimonial.text }}</p>
                        <span>{{ currentTestimonial.author }}</span>
                    </div>
                </div>
            </div>

            <div class="score-carousel">
                <span v-for="(currentTestimonial, index) in testimonials" :key="index" @click="changeSlide(index)"
                    :class="{ 'active': index === activeSlideIndex }"></span>
            </div>
        </div>

    </div>



</template>

<style lang="scss" scoped>
@use '../styles/mixins' as *;
@use '../styles/variables' as *;

#testimonials {

    font-family: "Poppins", sans-serif;
    
    position: relative;


    background-image: url('../../public/img/bg8.jpg');
    background-size: cover;

    #content-testimonials {
        @include styleContainer;

        padding: 115px 0;

        h3 {
            font-size: 35px;
            font-weight: 700;
            color: white;
        }


        button {
            background-color: $PrimaryColor;
            padding: 10px 15px;
        }

        img {
            width: 200px;
            height: 200px;
            border-radius: 50%;
            object-fit: cover;
        }
    }

}



#feedback {
    

    display: none;

    padding: 35px 25px;
    background-color: rgba(92, 117, 147, 0.668);

    color: white;

    &.active{
        display: block;
        display: flex;
        align-items: center;
        gap: 70px;
    }
    
    p {
        margin-bottom: 40px;
    
       
        } 
        
    //     &::before {
    //         content: '\f10e';
    //         font-family: 'Font Awesome';
           
    
    //         font-size: 24px;
    //         color: #000;
    // }
    
    span {
        font-weight: 700;
    }
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
</style>