<script>



export default {

    name: 'AppHistory',



    data() {
        return {

        }
    },


    methods: {

    },





}

</script>

<template>

    <div id="history">
        <img src="../../public/img/bg4.jpg" alt="">

        <div class="history-content  w-50 ">

            <div class="history-text">
                <div class="title">
                    <h2>Our History</h2>
                </div>

                <div class="score">
                    <div class="score-text"></div>
                </div>

                <div class="description">

                    <p>
                        <strong>Founded by a worldwide-famous yacht racer Alfred Tannenstrick,
                            since its inception back in 1977, this company has been a welcoming harbor for all
                            yachting and sailing enthusiasts, from all across the US!
                        </strong>
                    </p>

                    <p>We offer a real variety of professional services, from the simple yachts
                        chartering and corporate events, all the way to yacht repairs, upgrades and modifications and
                        maintenance checkups.
                    </p>

                    <p>With decades of professional experience in renting, repairing and transporting
                        just all kinds of yachts and boats under our belt - we can assure you that we are
                        your best choice!
                    </p>
                </div>

                <button class="btn btn-outline-light">Read More</button>
            </div>
        </div>
    </div>



</template>

<style lang="scss">
@use '../styles/mixins' as *;
@use '../styles/variables' as *;


#history {
    position: relative;
    font-family: "Poppins", sans-serif;
}

.history-content {
    position: absolute;
    top: 0;
    right: 0;

    padding-right: 120px;

    h2{
        font-weight: 700;
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
            left: 0;

            width: 100px;
            height: 1px;

            border-radius: 15px;
            background-color: $PrimaryColor;
        }
    }

    button {
        @include styleButton;

        &:hover {
            @include styleButtonHover;
        }
    }

    p {
        margin-bottom: 30px;
    }

    .history-text {
        margin-top: 120px;
    }

    p:not(:has(strong)) {
        color: #6e7077;
    }
}
</style>