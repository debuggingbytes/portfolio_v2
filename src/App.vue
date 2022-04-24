<template>
  <TopHeader />
  <router-view/>
  <SocialBar/>
</template>


<script>
import TopHeader from './components/layout/TopHeader'
import SocialBar from '@/components/layout/SocialBar'


export default {

  data() {
    return {
    }
  },

  components: {
    TopHeader,
    SocialBar,
  }


}

</script>
<style lang="scss">
  @import "./scss/main.scss"
</style>