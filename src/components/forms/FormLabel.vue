<template>
  <label for="{{forLabel}}" :class="css">{{label}}</label>
</template>

<script>
export default {
  props: ['label', 'forLabel', 'css']

}
</script>

<style>

</style>