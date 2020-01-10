<template>
 <section id="about">
   <h2> About me </h2>
   <p> Hello! I'm a front-end developer and I'm currently looking for an internship. I wish to create functional and inspirational websites for my future clients. Check out some of my <a href="#projects">projects</a> and don't hesitate to <a href="#contact">contact</a> if you would like to know more! </p>
 </section>
</template>

<script>
export default {
  name: 'About',
}
</script>

<style scoped>
section {
  display: flex;
  align-items: center;
  flex-direction: column;
}
p {
  line-height: 24px;
  max-width: 700px;
}
a {
  text-decoration: none;
}
</style>
