<script>

import AppNavBar from './AppNavBar.vue'

export default {

    name: 'AppHeader',

    components:{
        AppNavBar,
    },

    data(){
        return{
            links:[
                {
                    link:"About",
                },
                {
                    link:"Services",
                },
                {
                    link:"yachts",
                },
                {
                    link:"reservations",
                },
                {
                    link:"blog",
                },
                {
                    link:"contacts",
                },
            ]
        }
    }

  



}

</script>

<template>

<div id="hero">
    <img src="../../public/img/bg1-1.jpg" alt="">
    <div class="container">
        <AppNavBar :menuLinks="links"></AppNavBar>

    </div>
</div>

</template>

<style lang="scss">
@use '../styles/mixins' as *;
@use '../styles/variables' as *;

#hero{
    position: relative;
}
.container {
    @include styleContainer;

    

}
</style>