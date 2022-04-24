<template>
  <section id="portfolio-section" class="portfolio">
    <div class="portfolio__group">
      <div class="portfolio__header">
        <div class="row">
          <h2 class="h2 h2--orange txt-center">Portfolio</h2>
          <p class="portfolio--text pt-md pb-md">
          Here you can find some of my recent work.  Various projects for clients as well as some personal projects.
        </p>
        </div>
      </div>
      <div class="row">
        <PortfolioCard v-for="project in this.portfolio" :key="project.id" :project="project" />
      </div>
    </div>
  </section>
</template>
<script>

  import PortfolioCard from "./PortfolioCard"

  export default {
    data(){
      return {
        
      }   
    },
    components: {
      PortfolioCard
    },
    props: ['portfolio', 'project']
  }

</script>