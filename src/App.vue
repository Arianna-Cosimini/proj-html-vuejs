<script>

import AppTopBar from './components/AppTopBar.vue';
import AppHeader from './components/AppHeader.vue';
import AppHistory from './components/AppHistory.vue';
import AppService from './components/AppService.vue';
import AppYacht from './components/AppYacht.vue';


export default {

  components: {
    AppTopBar,
    AppHeader,
    AppHistory,
    AppService,
    AppYacht,
  }





}

</script>

<template>

<AppTopBar></AppTopBar>
<AppHeader></AppHeader>
<AppHistory></AppHistory>
<AppService></AppService>
<AppYacht></AppYacht>


</template>

<style lang="scss">

img{
  width: 100%;
}





</style>
