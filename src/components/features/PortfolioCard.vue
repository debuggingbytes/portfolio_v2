<template>
  <div class="col-1-of-4">
    <div class="card">
      <div class="card__side card__side--front">
        <div class="card__picture card__picture--1">
          &nbsp;
        </div>
        <h4 class="card__heading">
          <span class="card__heading-span card__heading-span--1">
            {{project.name}}

          </span>
        </h4>
        <div class="card__details">
          <p class="card__details--info txt-justify">{{project.details.info}}</p>
        </div>
      </div>
      <div class="card__side card__side--back card__side--back--1">
        <div class="card__cta">
          <div class="card__price-box">
            <h3 class="h3">Stacks</h3>
            <div class="card__details">
              <ul>
                <li v-for="stack in project.details.stacks" :key="stack.name">{{stack}}</li>
              </ul>
            </div>
            
          </div>
          <a :href="project.github" class="btn btn-white mx-sm">GitHub</a>
          <a :href="link" class="btn btn-white  mx-sm">DEMO</a>
        </div>
      </div>
    </div>
  </div>
</template>



<script>
export default {
  props: ['project'],
  data() {
    return {
      link: '',
    }
  },
  created(){
    this.project.demo ? this.link = this.project.demo : this.link = this.project.url
  },

}
</script>
