<script>
import bottomFooter from './bottomFooter.vue'


export default {

    name: 'AppFooter',

    components:{
        bottomFooter,
    },

    data() {
        return {

        }
    },


    methods: {

    },

    props: {
        footerLinks: Array,
    }


}

</script>

<template>
    <footer>
        <div id="content-footer">
            <div class="footer-logo">
                <img src="../../public/img/logo (1).png" alt="">
                <p>Yacht rentas for people who love sailing across the seas... </p>
            </div>

            <div id="footer-links" class="d-flex">
                <ul v-for="category in footerLinks" :key="category.title">
                    <li v-for="link in category.links" :key="link.text">
                        <a :href="link.url">{{ link.text }}</a>
                    </li>
                </ul>
            </div>
            <div id="newsletter">
                <h4>Newsletter</h4>

                <form>
                    <input type="text" placeholder="Enter your e-mail" class="border-0">
                    <button class="btn btn-outline-light ">Subcribe</button>
                </form>
            </div>

        </div>
    </footer>
    <bottomFooter></bottomFooter>
</template>

<style lang="scss">
@use '../styles/mixins' as *;
@use '../styles/variables' as *;

footer {
    background-color: #f5f5f5;
    padding: 140px 0;
}

#content-footer {
    @include styleContainer;
    display: flex;
    justify-content: space-between;





}

.footer-logo {
    img {
        width: 230px;
        margin-bottom: 30px;
    }
}

#footer-links {
    gap: 50px;

    ul {
        list-style: none;

        a {
            text-decoration: none;
            color: black;
            text-transform: uppercase;
            font-weight: 700;
        }
    }


}

#newsletter {

    h4 {
        font-weight: 700;
    }

    form {
        display: flex;
    }

    input {
        padding: 10px 15px;
    }

    button {
        @include styleButton;

        &:hover{
            @include styleButtonHover;
        }
    }
}
</style>