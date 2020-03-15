<template>
  <div id="app">
    <Home />
    <About />
    <Projects />
    <Contact />
    <Navigation />
  </div>
</template>

<script>
import Home from "../components/Home.vue";
import About from "../components/About.vue";
import Projects from "../components/Projects.vue";
import Contact from "../components/Contact.vue";
import Navigation from "../components/Navigation.vue";

export default {
  name: 'Index',
  components: {
      Home,
      About,
      Projects,
      Contact,
      Navigation,
  }
}
</script>

<style scoped>

</style>