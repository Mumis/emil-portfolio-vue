<template>
  <article>
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
  display: flex;
  flex-direction: column;
  justify-content: flex-end;
  padding: 30px 5px;
  text-align: center;
  height: 640px;
  width: 360px;
  background-image: linear-gradient(rgba(253,193,104,1)-50%, rgba(251,128,128,1));
}
article * {
  transform: skewY(-2deg);
  color: white;
}
p {
  font-size: 20px;
  margin: 40px 0;
  font-weight: lighter;
}
a > i {
  margin: 0 30px;
  font-size: 32px;
  transition: 0.2s;
}
a:hover > i {
  transform: scale(1.2);
}
</style>
