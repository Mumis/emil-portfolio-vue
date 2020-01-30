<template>
 <section id="about">
   <h2> About me </h2>
   <p>Hello! I'm a front-end developer and I'm currently looking for an internship. I wish to create functional and inspirational websites for my future clients. Check out some of my <a href="#projects">projects</a> and don't hesitate to <a href="#contact">contact</a> if you would like to know more!</p>
   <p>These are some of the <span class="highlighted">technologies</span> I have worked with:</p>
   <ul>
    <a href="https://reactjs.org/" target="_blank" rel="noopener noreferrer"><li><img :src="icons.react" alt="React icon" srcset=""><p>React.js</p></li></a>
    <a href="https://www.gatsbyjs.org/" target="_blank" rel="noopener noreferrer"><li><img :src="icons.gatsby" alt="Gatsby icon" srcset=""><p>Gatsby.js</p></li></a>
    <a href="https://vuejs.org/" target="_blank" rel="noopener noreferrer"><li><img :src="icons.vue" alt="Vue icon" srcset=""><p>Vue.js</p></li></a>
    <a href="http://firebase.google.com" target="_blank" rel="noopener noreferrer"><li><img :src="icons.firebase" alt="Firebase icon" srcset=""><p>Firebase</p></li></a>
    <a href="http://https://www.netlify.com/" target="_blank" rel="noopener noreferrer"><li><img :src="icons.netlify" alt="Netlify icon" srcset=""><p>Netlify</p></li></a>
    <a href="https://git-scm.com/" target="_blank" rel="noopener noreferrer"><li><img :src="icons.git" alt="Git icon" srcset=""><p>Git</p></li></a>
    <a href="http://https://github.com/" target="_blank" rel="noopener noreferrer"><li><img :src="icons.github" alt="Github icon" srcset=""><p>Github</p></li></a>
    <a href="https://threejs.org/" target="_blank" rel="noopener noreferrer"><li><img :src="icons.three" alt="Three icon" srcset=""><p>Three.js</p></li></a>
   </ul>
   <p>These are some of my favorite <span class="highlighted">tools</span>:</p>
   <ul>
    <a href="https://code.visualstudio.com/" target="_blank" rel="noopener noreferrer"><li><img :src="icons.vs" alt="VScode icon" srcset=""><p>Visual studio</p></li></a>
    <a href="https://www.adobe.com" target="_blank" rel="noopener noreferrer"><li><img :src="icons.photoshop" alt="VScode icon" srcset=""><p>Photoshop</p></li></a>
    <a href="https://www.adobe.com" target="_blank" rel="noopener noreferrer"><li><img :src="icons.xd" alt="VScode icon" srcset=""><p>Adobe XD</p></li></a>
    <a href="https://krita.org" target="_blank" rel="noopener noreferrer"><li><img :src="icons.krita" alt="Krita icon" srcset=""><p>Krita</p></li></a>
   </ul>
 </section>
</template>

<script>
import reactIcon from '../assets/icons/react.svg';
import gatsbyIcon from '../assets/icons/gatsby.svg';
import vueIcon from '../assets/icons/vue.svg';
import firebaseIcon from '../assets/icons/firebase.svg';
import netlifyIcon from '../assets/icons/netlify.svg';
import gitIcon from '../assets/icons/git.svg';
import githubIcon from '../assets/icons/github.svg';
import threeIcon from '../assets/icons/three.svg'
import vsIcon from '../assets/icons/vs.svg'
import photoshopIcon from '../assets/icons/photoshop.svg'
import xdIcon from '../assets/icons/xd.svg'
import kritaIcon from '../assets/icons/krita.svg'

export default {
  name: 'About',
  data: function() {
    return {
      icons: {
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
      }
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
  flex: 1 0 21%;
}
ul {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  text-align: left;
  list-style: none;
  padding: 0;
	width: 100%;
}
li {
    margin: 20px 20px;
    flex: 1 0 21%;
    text-align: center;
    transition: .3;
}
img {
  height: 50px;
  transition: opacity 0.3s;
}
li:hover img {
  opacity: .5;
}
</style>
