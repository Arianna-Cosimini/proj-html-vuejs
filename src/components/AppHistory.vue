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
}

.history-content {
    position: absolute;
    top: 0;
    right: 0;

    padding:0  120px;


    .score {
        background-color: #c1d3df;
        border-radius: 15px;
        height: 1px;

        position: relative;

        margin: 70px 0;

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
        background-color: $PrimaryColor;
        border-color: $PrimaryColor;

        padding: 10px 15px;

        font-weight: 700;
    }

    p {
        margin-bottom: 40px;
    }

    .history-text {
        margin-top: 165px;
    }

    p:not(:has(strong)){
        color: #6e7077;
    }
}
</style>