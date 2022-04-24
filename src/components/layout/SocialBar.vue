<template>
  <div class="socialBar">
    <div class="socialBar__vertical" v-if="this.socialVisible"></div>
      <h2 @click.prevent="toggleSocial" class="socialBar__show">
        <span class='btn-social'>{{this.socialVisible ? '&larr;' : '&rarr;' }}</span>
      </h2>
  
  </div>

</template>

<script>
export default {
  data() {
    return {
      socialVisible: true,

    }
  },

  methods: {
    toggleSocial(){
      return this.socialVisible = !this.socialVisible
    }
  }
}
</script>