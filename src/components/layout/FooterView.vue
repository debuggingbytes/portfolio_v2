<template>
  <footer class="footer">
    <div class="footer__body">
      <p>
        <span class="copyright">
          copyright &copy; {{date}} kriscartmell.com
        </span> 
        <span class="withLove">
          Website made with love from Canada.
        </span>
      </p>
    </div>
  </footer>
</template>

<script>
export default {
  data(){
    return {
      date: ''
    }
  },
  created(){
    const year = new Date();
    this.date = year.getFullYear();
  }

}
</script>

<style>

</style>