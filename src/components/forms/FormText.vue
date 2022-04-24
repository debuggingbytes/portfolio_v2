<template>
  <!-- {{message.length}} -->
  <textarea @keyup="checkText" v-model="message" :class="css" :placeholder="placeholder" required>

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
      maxChars: 50,
      error: '',
    }
  },
  components: {
    AlertBox
  },
  props: ['css', 'placeholder', 'alertMessage'],
  methods: {
    checkText() {
      if(this.message.length > this.maxChars){
        // alert("This is bad")
        this.error = "You've exceeded the maximum allowed characters, please reduce your message by " + (this.maxChars - this.message.length) + " characters."
        this.tooLong = true
      }else{
        this.tooLong = false
      }
      
    }
  }
}
</script>