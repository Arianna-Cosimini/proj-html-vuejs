<script>

import ServiceItems from './ServiceItems.vue'

export default {

    name: 'AppService',

    data() {
        return {
            services:[
                {
                    icon:"fa-solid fa-anchor",
                    title:"Yacht Rentals",
                    text:"With more than two hundred yacht and boat models on our fleet and both the East and the West Coasts covered, we are able to offer you the best yacht chartering options "
                },
                {
                    icon:"fa-regular fa-user",
                    title:"Management",
                    text:"On par with providing an amazing range of rentals on boats and yachts of all sizes and comfort levels, we will also gladly pick up on providing all kinds of maintenance... "
                },
                {
                    icon:"fa-solid fa-truck-fast",
                    title:"Transportation",
                    text:"Whenever any of our clients wants to try some brand new sailing destination or make a place of residence move to another water area - there comes the issue of logistics."
                },
                {
                    icon:"fa-regular fa-star",
                    title:"Yacht Repair",
                    text:"With decades of professional experienc in renting, repairing and transporting just all kinds of yachts and boats under our belt - we can assure you that we are your best choice"
                },
                {
                    icon:"fa-regular fa-thumbs-up",
                    title:"Yacht Rentals",
                    text:"As far as any personally - owned vehicles are concerned, whether we are alking about cars with four wheels, bikes with two wheels or yachts with no wheels, owners do.."
                },
                {
                    icon:"fa-solid fa-suitcase",
                    title:"Corporate Events",
                    text:"When it comes to organizing a corporate yacht charter of a Fortune 500 scale for a big crew o people - we will be able to make t flawless. We will exceed your expectations!"
                },
            ],
            
        }
    },


    methods: {

    },



    components: {
        ServiceItems,
    }



}

</script>

<template>

    <div id="service">
        <img src="../../public/img/bg5.jpg" alt="">

        <div id="service-content" class="d-flex flex-column justify-content-center align-items-center">

            <div class="service-text text-center">

                <h2>Yacht Charters, Repairs & Transportation, US - wide!</h2>
            </div>

            <div class="service-button">
                <button class="btn btn-outline-light">More Details</button>
            </div>
        </div>
    </div>

    <ServiceItems :CardItem="services"></ServiceItems>



</template>

<style lang="scss">
@use '../styles/mixins' as *;
@use '../styles/variables' as *;

#service {
    font-family: "Poppins", sans-serif;
    
    position: relative;
}

#service-content {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, - 50%);
    color: white;

    .service-text h2 {
        font-weight: 700;
        font-size: 55px;

        margin-bottom: 55px;
    }

    .service-button {
        button {
            @include styleButton;

            &:hover {
                @include styleButtonHover;
            }
        }
    }
}
</style>