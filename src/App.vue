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
    font-family: 'Montserrat', sans-serif;
  }
  body {
    margin: 0;
  }
  h1, h2, h3, p, small {
    margin: 0;
  }
</style>
