<template>
  <li>
    <img v-bind:src="project.image"/>
    <h3>{{project.title}}</h3>
    <p>{{project.text}}</p>
    <div>
      <a v-bind:href="project.page_url" target="_blank" rel="noopener noreferrer"><i class="fas fa-link"></i></a>
      <a v-bind:href="project.git_url" target="_blank" rel="noopener noreferrer"><i class="fab fa-github"></i></a>
    </div>
  </li>
</template>

<script>
export default {
  name: 'MainProject',
  props: {
    project: {
      required: true,
    }
  },
}
</script>

<style scoped>
li {
  overflow: hidden;
  position: relative;
  display: flex;
  flex-direction: column;
  justify-content: flex-end;
  text-align: center;
  width: 360px;
  height: 640px;
  padding: 0 5px;
  margin: 10px;
  background-image: linear-gradient(rgba(253,193,104,1)-50%, rgba(251,128,128,1));
  box-shadow: 0 1px 3px rgba(0,0,0,0.12), 0 1px 2px rgba(0,0,0,0.24);
  transition: box-shadow 0.3s cubic-bezier(.25,.8,.25,1);
}
li * {
  transform: skewY(-2deg);
  color: white;
}
li:hover {
  box-shadow: 0 14px 28px rgba(0,0,0,0.25), 0 10px 10px rgba(0,0,0,0.22);
}
li:hover > img {
  opacity: 0.9;
  mask-image: none;
}
li:hover > p, li:hover > h3 {
  display: none;
}
li:hover i {
  background: linear-gradient(rgba(253,193,104,1)-50%, rgba(251,128,128,1));
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}
img {
  position: absolute;
  top: -10px;
  left: 50%;
  width: 100%;
  max-width: 767px;
  opacity: 0.3;
  transform: translateX(-50%) skewY(-2deg);
  transition: 0.3s;
  mask-image: linear-gradient(to bottom, rgba(0,0,0,1), rgba(0,0,0,0));
}
p {
  font-size: 20px;
  font-weight: lighter;
  height: 10%;
  margin: 40px 0;
}
a > i {
  font-size: 32px;
  margin: 0 30px 60px 30px;
  transition: 0.2s;
}
a:hover > i {
  transform: scale(1.2);
}
@media only screen and (max-width: 767px) {
  li {
    width: 100%;
    margin: 0;
  }
  li:hover > img {
    opacity: 0.6;
    mask-image: linear-gradient(to bottom, rgba(0,0,0,1), rgba(0,0,0,0));
  }
  li:hover > p, li:hover > h3 {
    display: block;
  }
  li:hover i {
    color: white;
    background: none;
    -webkit-text-fill-color: inherit;
  }
}
</style>
