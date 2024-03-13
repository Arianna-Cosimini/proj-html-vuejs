<script>



export default {

    name: 'bottomFooter',



    data() {
        return {

        }
    },


    methods: {

    },



}

</script>

<template>
    <div id="bottom-footer">
        <div class="content-bottom-footer">
            <div class="policy">
                <ul>
                    <li><a href="#">zemez<span>@.all rights reserved</span></a></li>
                    <li><a href="#">privacy policy</a></li>
                    <li><a href="#">terms of use</a></li>
                </ul>
            </div>
            <div id="socials" class="d-flex">
                <div id="social-container" class="d-flex align-items-center justify-content-center">
                    <i class="fa-brands fa-facebook-f">
                        <a href="#"></a>
                    </i>
                </div>
    
                <div id="social-container" class="d-flex align-items-center justify-content-center">
                    <i class="fa-brands fa-twitter">
                        <a href="#"></a>
                    </i>
                </div>
    
                <div id="social-container" class="d-flex align-items-center justify-content-center">
                    <i class="fa-brands fa-instagram">
                        <a href="#"></a>
                    </i>
                </div>
    
    
            </div>
        </div>

    </div>
</template>

<style lang="scss">
@use '../styles/mixins' as *;
@use '../styles/variables' as *;


#bottom-footer {
    background-color: #222627;
    padding: 30px 0;
}

.content-bottom-footer {
    @include styleContainer;
    display: flex;
    justify-content: space-between;
}

.policy {
    ul {
        display: flex;

        span {
            color: #818075;
        }

        li {
            padding: 0 20px;
            border-right: 1px solid white;

            &:first-of-type {
                padding-left: 0;
            }

            &:last-of-type {
                border-right: 0;
            }
        }

    }

    a {
        text-decoration: none;
        color: white;
        text-transform: uppercase;
    }
}

#socials {

    gap: 20px;
    color: white;

    #social-container {
        width: 20px;
        height: 20px;
        border-radius: 50%;
        background-color: #6a6c71;

        i {
            font-size: 12px;
        }
    }


}
</style>