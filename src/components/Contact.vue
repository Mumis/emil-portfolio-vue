<template>
 <section id="contact">
   <h2>Contact</h2>
   <ul>
     <li>Emil Wertwein</li>
     <li>Åsögatan 191 / Stockholm / Sweden</li>
     <li>0700982746</li>
     <li>Emil.wertwein@gmail.com</li>
   </ul>
 </section>
</template>

<script>
export default {
  name: 'Contact',
}
</script>

<style scoped>
section {
  display: flex;
  flex-direction: column; 
  align-items: center;
}
ul {
  list-style: none;
  padding: 0;
}
li {
  color: rgb(74, 42, 24);
}
</style>
