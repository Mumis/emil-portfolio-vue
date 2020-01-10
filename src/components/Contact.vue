<template>
 <section id="contact">
   <h2>Contact</h2>
   <ul>
     <li><i class="fas fa-user"></i>Emil Wertwein</li>
     <li><i class="fas fa-home"></i>Åsögatan 191 / Stockholm / Sweden</li>
     <li><i class="fas fa-phone"></i>0700982746</li>
     <li><i class="fas fa-envelope"></i>Emil.wertwein@gmail.com</li>
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
  margin: 10px 0;
  color: rgb(74, 42, 24);
}
i {
  width: 20px;
  margin-right: 15px;
}
</style>
