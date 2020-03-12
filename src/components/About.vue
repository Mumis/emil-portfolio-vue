<template>
  <section id="about">
    <h2> About me </h2>
    <p>Hello! I'm a front-end developer and I'm currently looking for an internship. I wish to create functional and inspirational websites for my future clients.</p>
     
    <p>Check out some of my <a href="#projects">projects</a> and don't hesitate to <a href="#contact">contact</a> if you would like to know more!</p>
    <p>Some of the <span class="highlighted">technologies</span> and <span class="highlighted">tools</span> I have worked with:</p>
    <ul>
      <li v-for="icon in icons" v-bind:key=icon.key><Icon :icon="icon"/></li>
    </ul>
  </section>
</template>

<script>
import Icon from './AboutIcon';
import reactIcon from '../assets/icons/react.svg';
import gatsbyIcon from '../assets/icons/gatsby.svg';
import vueIcon from '../assets/icons/vue.svg';
import firebaseIcon from '../assets/icons/firebase.svg';
import netlifyIcon from '../assets/icons/netlify.svg';
import gitIcon from '../assets/icons/git.svg';
import githubIcon from '../assets/icons/github.svg';
import threeIcon from '../assets/icons/three.svg';
import vsIcon from '../assets/icons/vs.svg';
import photoshopIcon from '../assets/icons/photoshop.svg';
import xdIcon from '../assets/icons/xd.svg';
import kritaIcon from '../assets/icons/krita.svg';

export default {
  name: 'About',
  components: {
    Icon
  },
  data: function() {
    return {
      iconsImages: {
        react: reactIcon,
        gatsby: gatsbyIcon,
        vue: vueIcon,
        firebase: firebaseIcon,
        netlify: netlifyIcon,
        git: gitIcon,
        github: githubIcon,
        three: threeIcon,
        vs: vsIcon,
        photoshop: photoshopIcon,
        xd: xdIcon,
        krita: kritaIcon,
      },
      icons: [
        { name: "React.js", url: "https://www.reactjs.org/", img: reactIcon },
        { name: "Gatsby.js", url: "https://www.gatsbyjs.org/", img: gatsbyIcon },
        { name: "Vue.js", url: "https://www.vuejs.org/", img: vueIcon },
        { name: "Firebase", url: "https://www.firebase.google.com/", img: firebaseIcon },
        { name: "Netlify", url: "http://https://www.netlify.com/", img: netlifyIcon },
        { name: "Git", url: "https://git-scm.com/", img: gitIcon },
        { name: "Github", url: "http://https://github.com/", img: githubIcon },
        { name: "Three.js", url: "https://threejs.org/", img: threeIcon },
        { name: "Visual Studio", url: "https://code.visualstudio.com/", img: vsIcon },
        { name: "Photoshop", url: "https://www.adobe.com/", img: photoshopIcon },
        { name: "Adobe XD", url: "https://www.adobe.com/", img: xdIcon },
        { name: "Krita", url: "https://krita.org/", img: kritaIcon }
      ]
        
      
    }
  }
}
</script>

<style scoped>
section {
  display: flex;
  align-items: center;
  flex-direction: column;
	max-width: 700px;
	margin: auto;
}
p {
  line-height: 24px;
	align-self: flex-start;
}
a {
  text-decoration: none;
}
ul {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-evenly;
  text-align: left;
	width: 100%;
  list-style: none;
  padding: 0;
}
li {
    flex-basis: 25%;
  }
img {
  height: 56px;
  transition: opacity 0.3s;
}
@media only screen and (max-width: 767px) {
  li {
    flex-basis: 50%;
  }
}
</style>
