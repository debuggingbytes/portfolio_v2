<template>
  <!-- {{message.length}} -->
  <textarea @keyup="checkText" :id="forLabel" v-model="message" :class="css" :placeholder="placeholder" required no-resize>

  </textarea>
  <AlertBox css="alert alert-error" :alertMessage="error" v-if="tooLong"/>
 
</template>

<script>
import AlertBox from "../features/AlertBox"

export default {

  data() {
    return {
      tooLong: false,
      message: '',
      maxChars: this.textMax,
      error: '',
    }
  },
  components: {
    AlertBox
  },
  props: {
    css: {type: String},
    placeholder: {type: String},
    alertMessage: {type: String},
    textMax: {type: Number},
    forLabel: {type: String},
  },
  methods: {
    checkText() {
      if(this.message.length > this.maxChars){
        // alert("This is bad")
        this.error = "You've exceeded the maximum allowed characters [ "+ this.textMax +" ], please reduce your message by " + (this.maxChars - this.message.length) + " characters."
        this.tooLong = true
      }else{
        this.tooLong = false
      }
      this.$emit('catchValue', 'message', this.message )
      
    }
  }
}
</script>