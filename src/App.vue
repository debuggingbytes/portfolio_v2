<template>
  <div>
    <Transition name="fade-scale" key="0">
      <div v-if="resumeVisible">
       <ResumeView @event="resumeToggle" />
      </div>
    </Transition>
    <Transition name="slide-left">
      <div v-if="mobileNavVisible" style='z-index: 2998; position: relative;'>
        <MobileNav/>
      </div>
    </Transition>
    <TopHeader @event="resumeToggle" @navToggle="toggleMobileNav" />
    <router-view/>
    <SocialBar/>
    <FooterView />
  </div>
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
      mobileNavVisible: false,
    }
  },

  methods: {
    resumeToggle(){
      this.resumeVisible = !this.resumeVisible
      // console.log("working")
    },
    toggleMobileNav(){
      this.mobileNavVisible = !this.mobileNavVisible
      // console.log("Working Mobile nav")
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
