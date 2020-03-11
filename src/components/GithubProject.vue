<template>
  <li>
    <div>
        <h3>{{project.name}}</h3>
        <p>{{project.description}}</p>
    </div>
    <div>
      <a v-bind:href="project.html_url" target="_blank" rel="noopener noreferrer"><i class="fab fa-github"></i></a>
    </div>
  </li>
</template>

<script>
export default {
  name: 'GithubProject',
  props: {
    project: {
      required: true,
    }
  },
}
</script>

<style scoped>
li {
	display: flex;
	justify-content: space-between;
	align-items: center;
	width: 560px;
	padding: 10px 10px;
	margin: 10px;
	background-color: rgba(251,128,128,1);
}
li * {
	color: white;
}
div {
	transform: skewY(-2deg);
}
a > i {
  font-size: 32px;
  transition: 0.2s;
}
a:hover > i {
  transform: scale(1.2);
}
@media only screen and (max-width: 767px) {
	li {
		width: 100%;
		margin: 0;
		border-bottom: solid 2px white;
	}
}
</style>
