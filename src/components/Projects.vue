<template>
 <section id="projects">
   <ul>
     <li v-for="project in projects" v-bind:key=project.id> <project :project="project"/></li>
   </ul>
 </section>
</template>

<script>
import project from "./Project.vue";

export default {
  name: 'Projects',
  components: {
    project,
  },
  data: function() {
    return {
      projects: [
        { id: 0, title: "Smash Arenas", text: "An arena finder using firebase for the game Super Smash Bros. Ultimate.", page_url: "http://smasharenas.com", git_url: "https://github.com/Mumis/Smash-arenas", image:"dada"},
        { id: 1, title: "Personal blog", text: "A simple but elegant blog. All content can be customized with the integrated CMS.", page_url: "https://blog.emil.wertwein.com/", git_url: "https://github.com/Mumis/Simple-blog", image:"dada"},
        { id: 2, title: "Prometron", text: "A web multiplayer game, where players race against opponents whilst avoiding their tracks.", page_url: "https://prometron.wertwein.com/", git_url: "https://github.com/Mumis/EmilWertwein-Prometron", image:"dada"}
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
</style>