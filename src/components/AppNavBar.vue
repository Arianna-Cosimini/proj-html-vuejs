<script>


export default {

    name: 'AppNavBar',

    props: {
        menuLinks: Array,
    }



}

</script>

<template>

    <nav>
        <div class="container">

            <div id="navbar" class="d-flex justify-content-between align-items-center">
                <div class="img-nav">
                    <img src="../../public/img/logo.png" alt="">
                </div>
    
                <div id="menu-links" class="">
                    <ul class="d-flex list-unstyled ">
                        <li v-for="link in menuLinks" :key="link.link">
                            <a :href="'#' + link.link">{{ link.link }}</a>
                        </li>
                    </ul>
                </div>
    
                <div class="search">
                    <img src="../../public/img/image.svg" alt="">
                </div>
            </div>
        </div>

    </nav>

</template>

<style lang="scss">
@use '../styles/mixins' as *;
@use '../styles/variables' as *;

nav {
    font-family: "Poppins", sans-serif;
    
    position: absolute;
    width: 100%;
    left: 0;
    top: 35px;


    ul {
        gap: 48px;
        margin: 0;

        a {
            text-decoration: none;
            color: white;
            text-transform: uppercase;
            font-weight: 600;

            &:hover{
                color: $PrimaryColor;
            }
        }
    }

    .search {
        img {
            width: 20px;
        }
    }
}
</style>