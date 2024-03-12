<script>

import AppTopBar from './components/AppTopBar.vue';

import AppHeader from './components/AppHeader.vue';
import AppHistory from './components/AppHistory.vue';

import AppService from './components/AppService.vue';


export default {

  components: {
    AppTopBar,
    AppHeader,
    AppHistory,
    AppService,
  }





}

</script>

<template>

<AppTopBar></AppTopBar>
<AppHeader></AppHeader>
<AppHistory></AppHistory>
<AppService></AppService>


</template>

<style lang="scss">

img{
  width: 100%;
  height: 100%;
}

</style>
