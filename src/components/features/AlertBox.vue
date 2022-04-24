<template>
  <div :class="css">
    {{alertMessage}}
  </div>
</template>

<script>
export default {

  data(){
    return {

    }
  },
  props: ['css', 'alertMessage']

}
</script>