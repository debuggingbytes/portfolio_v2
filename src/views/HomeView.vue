<template>
  <main class="main">
    <section class="about">
      <div class="row">
        <div class="about-heading pb-lg">
          <h2 class="h2 h2--blue">About me</h2>
        </div>
        <div class="col-1-of-2">
          <p class="content pb-sm">
            I am a <span class="highlight">full stack</span> developer with a
            passion for thinking outside the box and learning the latest
            languages and frameworks. I started learning to code back in 2000, completely self-taught through trial and error, and have since refined my skills through various <a href='#bootcamps' @click="toggleBootcamp" class="highlight" :class="bootcampVisible ? '': 'grow'">Bootcamps</a>.
          </p>
          <p class="content">
            Fast forward {{ years }} years, I now have my own free lance
            business and found the time to become a certified mobile crane
            operator in the oil &amp; gas industry.
          </p>
        </div>
        <div class="col-1-of-2">
          <div class="stacks">
            <StackItem 
              v-for="lang in data.lang"
              :key="lang.id"
              :stack="lang.name"
            />
          </div>
        </div>
      </div>
      <div id="bootcamps">
        <Transition name="slide-fade" appear>
        <div class="row pt-md" v-if="bootcampVisible">
            <Bootcamp :courses="data.bootcamps" :bootcamp="toggleBootcamp"/>
        </div>
       </Transition>
      </div>
    </section>
    <PortfolioView :portfolio="data.portfolio" />
    <Transition name="fade-scale">
      <ContactForm v-show="contactVisible" @handleContact="toggleContact"/>
    </Transition>
  </main>
</template>

<script>
// @ is an alias to /src

import StackItem from '@/components/features/StackItem';
import PortfolioView from '@/components/features/PortfolioView';
import ContactForm from '@/components/features/ContactForm';
import Bootcamp from '@/components/features/BootcampItem';




export default {
  data() {
    return {
      years: this.getYear(),
      data: [],
      bootcampVisible: false,
      contactVisible: true
      
    }
  },
  components: {
    StackItem,
    PortfolioView,
    ContactForm,
    Bootcamp
  },
  props: ['stack', 'portfolio', 'courses', 'bootcamp', 'contactFunction'],
  methods: {
    getYear() {
      const year = new Date();
      return year.getFullYear() - 2000;
    },
    getData() {
      fetch('./assets/data.json')
        .then((res) => res.json())
        .then((data) => {
          // console.log(data);
         this.data = data;
        })
        .catch((err) => console.log(err));
    },
    toggleBootcamp(){
      this.bootcampVisible = !this.bootcampVisible
    },
    toggleContact(){
      this.contactVisible = !this.contactVisible
    }
  },
  mounted() {
    this.getData()
  }
}; // Export default data
</script>

<style>

</style>