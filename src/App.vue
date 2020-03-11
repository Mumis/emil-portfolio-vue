<template>
    <Index />
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
/* ---- GLOBAL STYLES ---- */
* {
  font-family: 'Ubuntu', sans-serif;
  color: rgb(178, 112, 78);
}
html {
  scroll-behavior: smooth;
}
body {
  position: relative;
  margin: 0;
}
h1,h2,h3,h4 {
  font-weight: normal;
  font-family: 'Montserrat', sans-serif;
  font-weight: 300;
  color: rgb(74, 42, 24);
  margin: 0;
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
p {
  font-size: 16px;
}
a, i {
  color: #4A2A18;
}
section {
  padding: 80px 20px;
}
.highlighted {
  color: rgb(74, 42, 24);
}
</style>
