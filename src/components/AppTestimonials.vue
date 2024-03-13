<script>



export default {

    name: 'AppTestimonials',



    data() {
        return {

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

    },






}

</script>

<template>

    <div id="testimonials">
        <div id="content-testimonials" class="text-center">
            <h3>Testimonials</h3>

            <div class="score">
                <div class="score-text"></div>
            </div>


            <div v-for="currentTestimonial in testimonials" id="feedback"
                class="text-start mx-5 d-flex align-items-center gap-5 pe-5">
                <div class="img-testimonial">
                    <img :src="currentTestimonial.image" alt="">
                </div>

                <div class="text-testimonial">
                    <p>{{ currentTestimonial.text }}</p>
                    <span>{{ currentTestimonial.author }}</span>
                </div>
            </div>
        </div>

    </div>



</template>

<style lang="scss">
@use '../styles/mixins' as *;
@use '../styles/variables' as *;

#testimonials {


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

    #feedback {

        padding: 35px 25px;
        background-color: rgba(92, 117, 147, 0.668);

        color: white;

        p {
            margin-bottom: 40px;

            &::before {
                content: '\f10e';
                font-family: 'Font Awesome';
                /* Assicurati di avere caricato il font che contiene questo carattere */
                display: inline-block;
                font-size: 24px;
                /* Imposta la dimensione desiderata per l'icona */
                color: #000;
            }
        }

        span {
            font-weight: 700;
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
</style>