<script>



export default {

    name: 'ServiceItems',



    data() {
        return {

        }
    },


    methods: {

    },

    props: {
        CardItem: Array,
    }





}

</script>

<template>

    <div id="service-item">
        <div id="content-service-item" class="text-center">
            <h3>Services</h3>

            <div class="score">
                <div class="score-text"></div>
            </div>


            <div id="cards-item-service" class="d-flex flex-wrap ">
                <div v-for="items in CardItem" class="card-item px-4">
                    <div id="icon-card" class="d-flex align-items-center ">
                        <div class="icon">
                            <i :class="items.icon"></i>
                        </div>
                        <h4>{{ items.title }}</h4>
                    </div>

                    <div class="text-card text-start">
                        <p>{{ items.text }}</p>
                    </div>
                </div>
            </div>
        </div>
    </div>



</template>

<style lang="scss">
@use '../styles/mixins' as *;
@use '../styles/variables' as *;

#service-item {


    background-size: contain;
    background-position: bottom;
    background-image: url('../../public/img/bg6.jpg');

    #content-service-item {
        @include styleContainer;

        padding: 115px 0;

        h3 {
            font-size: 35px;
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

#icon-card {
    gap:30px;
    margin-bottom: 30px;
    
}

.card-item {
    width: calc(100% / 3);
    margin-bottom: 80px;


    .icon {

        display: flex;
        justify-content: center;
        align-items: center;

        width: 90px;
        height: 90px;
        border-radius: 50%;
        background-color: $PrimaryColor;

        i {
            color: white;
            font-size: 50px;
        }
    }
}
</style>