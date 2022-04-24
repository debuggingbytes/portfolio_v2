<template>
  <input :type="type" :class="css" :placeholder="placeholder" required/>
</template>

<script>
export default {

  props: ['type', 'css', 'placeholder']

}
</script>
