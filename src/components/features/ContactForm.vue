<template>
  <section id="contact-me" class="contact-me">
    <div class="contact-me__body">
      <div class="row">
        <h2 class="h2 h2--blue">Contact me</h2>
        <p class="pt-md">Lorem ipsum dolor sit amet consectetur adipisicing elit. Consectetur temporibus earum veritatis fugit maiores, reiciendis minima praesentium optio minus explicabo. Error odit, corrupti impedit tempore porro, amet aliquam sunt optio rem necessitatibus eum sapiente earum reiciendis tenetur qui, dolores quae consequuntur non atque recusandae neque. Voluptates qui veniam earum amet?</p>
      </div>
      <div class="row">
        <div class="contact-me__form" v-show="!formSent">
          <form @submit.prevent="submitContact">
            <FormGroup>
              <FormLabel css="form-label" label="Full Name" />
              <FormInput type="text" css="form-control" placeholder="John Smith" />
            </FormGroup>
            <FormGroup>
              <FormLabel css="form-label" label="Email" />
              <FormInput type="email" css="form-control" placeholder="email@example.com"/>
            </FormGroup>
            <FormGroup>
              <FormLabel css="form-label" label="Your Message" />
              <FormText css="form-control-text" placeholder="Hey I wanted to ... "/>
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
      formSent: false,
    }
  },
  components: {
    FormGroup, FormInput, FormLabel, FormButton, FormText
  },
  props: [
    
    'type', 'css', 'text', 'placeholder',
    // Label Props
    'label', 'forLabel'
    ],
  methods: {
    submitContact() {
      alert('hello')
    }
  }

}
</script>