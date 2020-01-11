<template>
 <section id="projects">
  <ul>
    <li v-for="project in projects" v-bind:key=project.id> <project :project="project"/></li>
  </ul>
  <!-- <a>Like what you see? Check out my other projects!</a> -->
 </section>
</template>

<script>
import project from "./Project.vue";
import smasharenas from "../assets/smash-arenas.png";
import personalblog from "../assets/personal-blog.png";

export default {
  name: 'Projects',
  components: {
    project,
  },
  data: function() {
    return {
      projects: [
        { id: 0, title: "Smash Arenas", text: "An arena finder using firebase for the game Super Smash Bros. Ultimate.", page_url: "http://smasharenas.com", git_url: "https://github.com/Mumis/Smash-arenas", image:smasharenas},
        { id: 1, title: "Personal blog", text: "A simple but elegant blog. All content can be customized with the integrated CMS.", page_url: "https://blog.emil.wertwein.com/", git_url: "https://github.com/Mumis/Simple-blog", image:personalblog},
        { id: 2, title: "Prometron", text: "A web multiplayer game, where players race against opponents whilst avoiding their tracks.", page_url: "https://prometron.wertwein.com/", git_url: "https://github.com/Mumis/EmilWertwein-Prometron", image:personalblog}
      ]
    }
  },
}
</script>

<style scoped>
section {
  background-color: rgb(255, 218, 208);
	transform: skewY(2deg);
  box-shadow: inset 0px -25px 25px -25px rgba(0,0,0,0.50), inset 0px 25px 25px -25px rgba(0,0,0,0.50);
}
ul {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-evenly;
  list-style: none;
  padding: 0;
  margin: 0;
}
li {
  width: 360px;
  margin: 10px 0;
}
@media only screen and (max-width: 767px) {
  section {
    padding: 0;
  }
  li {
    width: 100%;
    margin: 0;
  }
}
</style>