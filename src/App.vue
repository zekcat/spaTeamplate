<template>
<div>
  <header-component></header-component>
  <about-us></about-us>
  <services-component></services-component>
  <latest-work></latest-work>
  <the-team></the-team>
  <testimonial></testimonial>
  <footer-section></footer-section>
</div>
</template>

<script>
import HeaderComponent from './components/HeaderComponent.vue';
import AboutUs from './components/AboutUs.vue';
import ServicesComponent from './components/ServicesComponent.vue';
import LatestWork from './components/LatestWork.vue';
import TheTeam from './components/TheTeam.vue';
import Testimonial from './components/Testimonial.vue';
import FooterSection from './components/FooterSection.vue';

export default {
  name: 'App',
  components: {
    HeaderComponent,
    AboutUs,
    ServicesComponent,
    LatestWork,
    TheTeam,
    Testimonial,
    FooterSection,
  },
};

</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Open+Sans:ital,wght@0,300;0,400;0,600;0,700;1,700&display=swap');
@import url("https://fonts.googleapis.com/css2?family=Oswald:wght@300;400;500&display=swap");

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  max-width: 1900px;
}
</style>
