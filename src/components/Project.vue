<template>
  <article>
    <img v-bind:src="project.image"/>
    <h3>{{project.title}}</h3>
    <p>{{project.text}}</p>
    <div>
      <a v-bind:href="project.page_url" target="_blank" rel="noopener noreferrer"><i class="fas fa-link"></i></a>
      <a v-bind:href="project.git_url" target="_blank" rel="noopener noreferrer"><i class="fab fa-github"></i></a>
    </div>
  </article>
</template>

<script>
export default {
  name: 'Project',
  props: {
    project: {
      required: true,
    }
  },
}
</script>

<style scoped>
article{
  overflow: hidden;
  position: relative;
  display: flex;
  flex-direction: column;
  justify-content: flex-end;
  padding: 0 5px;
  text-align: center;
  height: 640px;
  background-image: linear-gradient(rgba(253,193,104,1)-50%, rgba(251,128,128,1));
}
article * {
  transform: skewY(-2deg);
  color: white;
}
img {
  position: absolute;
  top: -10px;
  left: 50%;
  transform: translateX(-50%) skewY(-2deg);
  max-width: 767px;
  width: 100%;
  opacity: 0.6;
  transition: 0.3s;
  mask-image: linear-gradient(to bottom, rgba(0,0,0,1), rgba(0,0,0,0));
}
article:hover > img {
  opacity: 0.9;
  mask-image: none;
}
article:hover > p, article:hover > h3 {
  display: none;
}
article:hover i {
  background: linear-gradient(rgba(253,193,104,1)-50%, rgba(251,128,128,1));
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}
p {
  font-size: 20px;
  margin: 40px 0;
  font-weight: lighter;
}
a > i {
  margin: 0 30px 60px 30px;
  font-size: 32px;
  transition: 0.2s;
}
a:hover > i {
  transform: scale(1.2);
}
@media only screen and (max-width: 767px) {
  article:hover > img {
    opacity: 0.6;
    mask-image: linear-gradient(to bottom, rgba(0,0,0,1), rgba(0,0,0,0));
  }
  article:hover > p, article:hover > h3 {
    display: block;
  }
}
</style>
