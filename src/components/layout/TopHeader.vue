<template>
  <header class="header">
    <!-- 
      Header will have our hero image and navigation

      Start with hero
     -->
    <div class="hero">
      <div class="cta">
        <h1 class="h1">
          <span class="h1--sm">
            Hello,
          </span>
          I am Kris Cartmell
          <span class="h1--sm">
            a full stack developer
          </span>
        </h1>
        <!-- cta btn -->
        <div class="cta-btn">
          <a href="#" class="btn btn-orange">Learn More</a>
        </div>
        <!-- cta btn -->
      </div>
      <!-- end cta -->
    </div> 
    <!-- Hero -->
    <!-- start nav -->
    <nav class="nav-bar">
      <div class="nav-bar__logo">
        <img src="../../assets/img/icon.png" class="nav-bar__img" />
      </div>
      <div class="nav-bar__links">
        <ul class="nav-links">
          <li class="nav-link"><a href='' class="nav-link__link">Home</a></li>
          <li class="nav-link"><a href='' class="nav-link__link">ABout</a></li>
          <li class="nav-link"><a href='' class="nav-link__link">Portfolio</a></li>
          <li class="nav-link"><a href='' class="nav-link__link">Contact</a></li>
          <li class="nav-link"><a href='#resume' @click.prevent="this.$emit('event')" class="nav-link__link">resume</a></li>
        </ul>
      </div>
      <div class="nav-bar__mobile">
        <a class="nav-bar__mobile--btn" @click.prevent="this.$emit('navToggle')">&nbsp;</a>
      </div> 
    </nav>
  </header>
</template>

<script>
export default {
  name: "TopHeader",
  data() {
    return {
    };
  },
};
</script>
