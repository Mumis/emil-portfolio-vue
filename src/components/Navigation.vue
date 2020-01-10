<template>
  <nav>
    <img />
    <div>
      <a href="#home">Home</a>
      <a href="#about">About</a>
      <a href="#projects">Projects</a>
      <a href="#contact">Contact</a>
    </div>
  </nav>
</template>

<script>
export default {
  name: 'Navigation',
}
</script>

<style scoped>
nav {
  display: flex;
  justify-content: space-between;
  position: fixed;
  width: 100%;
  margin: 0;
  top: 20px;
}
a {
  font-size: 22px;
  font-weight: lighter;
  text-decoration: none;
  margin: 0 20px;
}
a:hover {
  color: rgb(178, 112, 78); 
}
</style>
