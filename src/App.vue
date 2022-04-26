<template>
  <Transition name="fade-scale">
    <ResumeView v-if="resumeVisible" @event="resumeToggle" />
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




export default {

  data() {
    return {
      resumeVisible: false,
    }
  },

  methods: {
    resumeToggle(){
      this.resumeVisible = !this.resumeVisible
      console.log("working")
    }
  },

  components: {
    TopHeader,
    SocialBar,
    FooterView,
    ResumeView,
  }


}

</script>
