<template>
  <div class="bootcamp">
    <h2 class="h2 h2--blue">Bootcamps</h2>
    <p class="pt-md">To keep up with the latest best practices, frameworks and stacks, Bootcamps felt like the best option.  With no real technical training, I was being over looked by potential employers. So I took the steps to enroll in <a class='highlight'>Udemy</a> bootcamps to give myself certificates and credentials to show future employers. I am proud to say I have greatly increased my frontend development skills.</p>
    <p class='pt-sm'>Below is the current list of completed bootcamps.
    </p>
    
    <div class="bootcamp__card" v-for="course in courses" :key="course.id">
      <div class="bootcamp__image">
        <h3 class="bootcamp__heading">{{course.name}}</h3>
      </div>
      <div class="bootcamp__body">
        {{course.details}}
      </div>
      <div class="bootcamp__footer">
        <div class="bootcamp__footer--text">
          <a href='#' @click.prevent="bootcamp" class=' '>Certificate</a>
        </div>
      </div>
    </div> 
  </div>
</template>

<script>

export default {
  data(){
    return {

    }
  },
  props: ['courses', 'bootcamp'],
  components: {
  }

}
</script>

