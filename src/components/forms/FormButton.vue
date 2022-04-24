<template>
  <button :class="css" :type="type">
    {{text}}
  </button>
</template>

<script>
export default {
  props: ['css', 'text', 'type']

}
</script>