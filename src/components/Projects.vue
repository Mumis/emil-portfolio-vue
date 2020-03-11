<template>
 <section id="projects">
  <ul v-if="!showAll">
    <mainProject v-for="project in mainProjects" v-bind:key=project.key :project="project"/>
  </ul>
  <ul v-else>
    <githubProject v-for="project in githubProjets" v-bind:key=project.key :project="project"/>
  </ul>
  <button v-if="!showAll" v-on:click="this.toggleAll">View my github projects</button>
  <button v-else v-on:click="this.toggleAll">View my latest projects</button>
 </section>
</template>

<script>
import mainProject from "./MainProject.vue";
import githubProject from "./GithubProject.vue";
import smasharenas from "../assets/smash-arenas.png";
import personalblog from "../assets/personal-blog.png";
import threeMinecraft from "../assets/three-minecraft.png";

export default {
  name: 'Projects',
  components: {
    mainProject,
    githubProject
  },
  data: function() {
    return {
      showAll: false,
      mainProjects: [
        { id: 0, title: "Smash arenas", text: "An arena finder using firebase for the game Super Smash Bros. Ultimate.", page_url: "http://smasharenas.com", git_url: "https://github.com/Mumis/Smash-arenas", image:smasharenas},
        { id: 1, title: "Personal blog", text: "A simple but elegant blog. All content can be customized with the integrated CMS.", page_url: "https://blog.emil.wertwein.com/", git_url: "https://github.com/Mumis/Simple-blog", image:personalblog},
        { id: 2, title: "Worlds in three.js", text: 'A voxel based "minecraft-like" browser game with randomly generated worlds.', image:threeMinecraft}
      ],
      githubProjets: null,
    }
  },
  methods: {
    toggleAll: async function() {
      this.showAll = !this.showAll;
    }
  },
  updated() {
    document.getElementById("projects").scrollIntoView();
  },
  created() {
    fetch("https://api.github.com/users/mumis/repos")
      .then((response) => response.json())
      .then((data) => this.githubProjets = data).then(() => console.log(this.githubProjets));
  }
}
</script>

<style scoped>
section {
  display: flex;
  flex-direction: column;
  align-items: center;
  background-color: rgb(255, 218, 208);
	transform: skewY(2deg);
  box-shadow: inset 0px -25px 25px -25px rgba(0,0,0,0.50), inset 0px 25px 25px -25px rgba(0,0,0,0.50);
}
ul {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  list-style: none;
  padding: 0;
  margin: 0;
  width: 100%;
  max-width: 1920px;
}
a {
  position: absolute;
  bottom: 20px;
  transform: skewY(-2deg);
  color: rgb(178, 112, 78);
}
a:hover {
  cursor: pointer;
}
a:hover .highlighted {
  transform: scale(2);
}
button {
  font-size: 20px;
  margin-top: 30px;
  transform: skewY(-2deg);
  color: rgb(74, 42, 24);
  background-color: inherit;
  border: none;
  cursor: pointer;
  transition: .2s;
}
button:hover {
  color: rgb(178, 112, 78);
}
@media only screen and (max-width: 767px) {
  section {
    padding: 0;
    box-shadow: none;
    background-color: white;
  }
  a {
    display: none;
  }
}
</style>