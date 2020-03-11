<template>
 <section id="contact">
  <h2>Contact</h2>
  <ul>
    <li><i class="fas fa-user"></i>Emil Wertwein</li>
    <li><i class="fas fa-home"></i>Åsögatan 191 / Stockholm / Sweden</li>
    <li><i class="fas fa-phone"></i>0700982746</li>
    <li><i class="fas fa-envelope"></i>Emil.wertwein@gmail.com</li>
  </ul>
  <div class="social-container">
    <a href="https://github.com/Mumis" target="_blank" rel="noopener noreferrer"><i class="fab fa-github"></i></a>
    <a href="https://www.linkedin.com/in/emilwertwein/" target="_blank" rel="noopener noreferrer"><i class="fab fa-linkedin-in"></i></a>
    <a href="https://twitter.com/wertwein" target="_blank" rel="noopener noreferrer"><i class="fab fa-twitter"></i></a>	
  </div>
  <small> Copyright &copy; 2020 Emil Wertwein </small>
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
  padding-bottom: 0;
}
ul {
  list-style: none;
  padding: 0;
}
li {
  margin: 15px 0;
  color: rgb(74, 42, 24);
}
i {
  width: 20px;
  margin-right: 15px;
}
.social-container i {
	margin: 0 30px;
	font-size: 25px;
	transition: color .2s;
}
.social-container i:hover {
	color: #B2704E;
}
small {
  font-size: 14px;
  margin: 30px 0;
}
</style>
