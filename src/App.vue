<template>
  <div id="app">
    <Index />
  </div>
</template>

<script>
import Index from './pages/Index.vue';

export default {
  name: 'app',
  components: {
    Index
  }
}
</script>

<style>
  * {
    font-family: 'Ubuntu', sans-serif;
  }
  body {
    margin: 0;
  }
  h1,h2,h3,h4 {
    color: rgb(74, 42, 24);
    font-weight: normal;
    margin: 0;
    font-family: 'Montserrat', sans-serif;
    font-weight: lighter;
  }
  h1 {
    font-size: 45px;
  }
  h2 {
    font-size: 35px;
  }
  h3 {
    font-size: 30px;
  }
  h4 {
    font-size: 25px;
  }
  p,small {
    color: rgb(178, 112, 78);
  }
</style>
