<script>


export default {

    name: 'AppTopBar',



}

</script>

<template>

    <div id="top-bar">
        <div class="container">
            <div id="contacts" class="d-flex justify-content-between">
                <div id="address">
                    <div class="place"></div>
                    <div class="number"></div>
                </div>

                <div id="socials">

                </div>
            </div>

        </div>
    </div>

</template>

<style lang="scss">
@use '../styles/mixins' as *;
@use '../styles/variables' as *;


.container{
    @include styleContainer
}
</style>