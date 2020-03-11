<template>
  <nav v-bind:class="{ open: open }">
    <img v-bind:src="logo"/>
      <span v-on:click="open = !open" id="hamburger"></span>
      <a v-on:click="open = !open" href="#home">Home</a>
      <a v-on:click="open = !open" href="#about">About</a>
      <a v-on:click="open = !open" href="#projects">Projects</a>
      <a v-on:click="open = !open" href="#contact">Contact</a>
  </nav>
</template>

<script>
import logo from "../assets/logo.png";

export default {
  name: 'Navigation',
  data: function() {
    return {
      open: false,
      logo: logo
    }
  }
}
</script>

<style scoped>
nav {
  position: fixed;
  width: 100%;
  top: 0;
  right: 0;
  padding-top: 20px;
  display: flex;
  justify-content: flex-end;
  transition: transform 200ms cubic-bezier(.5, 0, .5, 1);
}
img {
  display: none;
  height: 100px;
  width: 100px;
  opacity: .8;
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
#hamburger {
  display: none;
  position: absolute;
  bottom: 60px;
  left: 0;
  transform: translateX(-100%);
  background: white;
  border: solid white 16px;
  border-right: solid white 7px;
  border-left: solid white 7px;
  border-radius: .25em 0 0 .25em;
  cursor: pointer;
  box-shadow: 0 1px 3px rgba(202, 189, 189, 0.12), 0 1px 2px rgba(0,0,0,0.24);
  width: 22px;
  height: 3px;
  background: #4A2A18;
  transition: 100ms, transform 200ms ease-in-out, background 300ms linear;
}
#hamburger:before {
  content: '';
  position: absolute;
  right: 0;
  width: 18px;
  height: 3px;
  background: #4A2A18;
  transition: transform 500ms ease-in-out;
  bottom: 6px;
}
#hamburger:after {
  content: '';
  position: absolute;
  right: 0;
  width: 18px;
  height: 3px;
  background: #4A2A18;
  transition: transform 500ms ease-in-out;
  top: 6px;
}
@media only screen and (max-width: 767px) {
  #hamburger {
    display: block;
  }
  nav {
    flex-direction: column;
    justify-content: space-evenly;
    align-items: center;
    box-shadow: 0 0 1em rgba(0,0,0,.2);
    height: 100%;
    width: 80vw;
    padding: 0;
    transform: translateX(100%);
    background-color: white;
  }
  .open {
    transform: translateX(0);
  }
  img {
    display: block;
  }
}
</style>
