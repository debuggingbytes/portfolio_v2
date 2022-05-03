<template>
  <section id="contact-me" class="contact-me">
    <div class="contact-me__body">
      <div class="row">
        <h2 class="h2 h2--blue">Contact me</h2>
        <p class="pt-md">I would like to take the time to say thank you for visiting my portfolio site.  If you've made it this far down the page, please leave me a message with the form below.  I would love to hear where you are visiting from and how you found my page.</p>
      </div>
      <div class="row">
        <div class="contact-me__form">
          <form @submit.prevent="submitContact">
            <FormGroup>
              <FormLabel css="form-label" label="Full Name" forLabel="fullName" />
              <FormInput type="text" css="form-control" forLabel="fullName" placeholder="John Smith" />
            </FormGroup>
            <FormGroup>
              <FormLabel css="form-label" label="Email" forLabel="email" />
              <FormInput type="email" css="form-control" forLabel="email" placeholder="email@example.com"/>
            </FormGroup>
            <FormGroup>
              <FormLabel css="form-label" label="Your Message" forLabel="msg" />
              <FormText css="form-control-text" :textMax=500 forLabel="msg" placeholder="Hey I wanted to ... "/>
            </FormGroup>
            <FormGroup>
              <FormButton text="Submit Form" css="btn btn-blue" />
            </FormGroup>

          </form>
        </div>
      </div>
    </div>
  </section>
</template>

<script>

import FormGroup from '../forms/FormGroup'
import FormInput from '../forms/FormInput'
import FormLabel from '../forms/FormLabel'
import FormButton from '../forms/FormButton'
import FormText from '../forms/FormText'





export default {
  data(){
    return {
      fullName: '',
      email: '',
      message: '',
    }
  },
  components: {
    FormGroup, FormInput, FormLabel, FormButton, FormText
  },
  props: [
    
    'type', 'css', 'text', 'placeholder', 'textMax',
    // Label Props
    'label', 'forLabel',
    //passed methds
    'contactFunction',
    //Form Values
    'inputValue'
    ],
  methods: {
    submitContact() {
      console.log("Function fired")
      this.$emit('handleContact')
      setTimeout(() => {
        this.$emit('handleContact');
        console.log("function fired x3")
        }, 5500)

    },
  }

}
</script>