<script>

import AppTopBar from './components/AppTopBar.vue';
import AppHeader from './components/AppHeader.vue';
import AppHistory from './components/AppHistory.vue';
import AppService from './components/AppService.vue';
import AppYacht from './components/AppYacht.vue';
import AppEvents from './components/AppEvents.vue';
import AppBlog from './components/AppBlog.vue'

export default {

  components: {
    AppTopBar,
    AppHeader,
    AppHistory,
    AppService,
    AppYacht,
    AppEvents,
    AppBlog,
  }





}

</script>

<template>

<AppTopBar></AppTopBar>
<AppHeader></AppHeader>
<AppHistory></AppHistory>
<AppService></AppService>
<AppYacht></AppYacht>
<AppEvents></AppEvents>
<AppBlog></AppBlog>


</template>

<style lang="scss">

img{
  width: 100%;
}





</style>
