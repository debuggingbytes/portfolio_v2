<template>
  <Transition name="fade-scale">
    <ResumeView v-if="resumeVisible" @event="resumeToggle" />
  </Transition>
  <Transition name="fade-scale">
    <MobileNav v-if="mobileNavVisible" />
  </Transition>
  <TopHeader @event="resumeToggle" />
  <router-view/>
  <SocialBar/>
  <FooterView />
</template>


<script>
import TopHeader from './components/layout/TopHeader'
import SocialBar from '@/components/layout/SocialBar'
import FooterView from '@/components/layout/FooterView'
import ResumeView from '@/components/layout/ResumeView'
import MobileNav from '@/components/layout/MobileNav'





export default {

  data() {
    return {
      resumeVisible: false,
      navigationLinks: [],
      mobileNavVisible: true,
    }
  },

  methods: {
    resumeToggle(){
      this.resumeVisible = !this.resumeVisible
      // console.log("working")
    },
    toggleMobileNav(){
      this.moblileNavVisible = !this.mobileNavVisible
    }
  },

  components: {
    TopHeader,
    SocialBar,
    FooterView,
    ResumeView,
    MobileNav,
  }


}

</script>
