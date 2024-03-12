<script>


export default {

    name: 'AppEvents',

    data() {
        return {


        }
    },


    methods: {

    },




}

</script>

<template>

    <div id="event" class="d-flex align-items-center">

        <div id="event-content">

            <div class="event-text w-50">

                <h2>ENJOY</h2>
                <h3>WORLD RALLY 2017-19</h3>

                <p>Explore some of the most beautiful regions of the world. Make your dreams
                    come true and join the Yachtec Worls Rally 2017-19
                </p>
            </div>

            <div class="event-button">
                <button class="btn btn-outline-light">More Details</button>
            </div>
        </div>
    </div>



</template>

<style lang="scss" scoped>
@use '../styles/mixins' as *;
@use '../styles/variables' as *;

#event {

    min-height: 780px;
    // padding-left: 200px;
    // padding-top: 120px;

    background-image: url('../../public/img/bg7.jpg');
    background-size: cover;

}

#event-content {
    @include styleContainer;
    // transform: translatey(50%);

    

    color: white;

    .event-text{

        margin-bottom: 50px;

        h2 {
            font-weight: 700;
            font-size: 85px;
        }
    
        h3{
            font-size: 50px;
        }
    }
    
    

    .event-button {
        button {
            background-color: $PrimaryColor;
            border-color: $PrimaryColor;

            color: white;
            padding: 10px 15px;

            font-weight: 700;
        }
    }
}
</style>