<script>



export default {

    name: 'AppService',



    data() {
        return {

        }
    },


    methods: {

    },





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



</template>

<style lang="scss">
@use '../styles/mixins' as *;
@use '../styles/variables' as *;

#service {
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
            background-color: $PrimaryColor;
            border-color: $PrimaryColor;

            color: white;
            padding: 10px 15px;

            font-weight: 700;
        }
    }
}
</style>