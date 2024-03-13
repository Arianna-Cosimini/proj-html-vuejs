<script>

import AppTopBar from './components/AppTopBar.vue';
import AppHeader from './components/AppHeader.vue';
import AppHistory from './components/AppHistory.vue';
import AppService from './components/AppService.vue';
import AppYacht from './components/AppYacht.vue';
import AppEvents from './components/AppEvents.vue';
import AppBlog from './components/AppBlog.vue'
import AppTestimonials from './components/AppTestimonials.vue'
import AppFooter from './components/AppFooter.vue'

export default {

  components: {
    AppTopBar,
    AppHeader,
    AppHistory,
    AppService,
    AppYacht,
    AppEvents,
    AppBlog,
    AppTestimonials,
    AppFooter,
  },

  data() {
    return {
      footerLinksList: [
                {
                    title: 'part-1',
                    links: [
                        { text: 'yachts', url: '#' },
                        { text: 'services', url: '#' },
                        { text: 'reservations', url: '#' }
                    ]
                },
                {
                    title: 'part-2',
                    links: [
                        { text: 'blog', url: '#' },
                        { text: 'privacy policy', url: '#' },
                        { text: 'terms of use', url: '#' }
                    ]
                }
            ]
    }
  },





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
<AppTestimonials></AppTestimonials>
<AppFooter :footerLinks="footerLinksList"></AppFooter>

</template>

<style lang="scss">

img{
  width: 100%;
}





</style>
