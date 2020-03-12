<template>
  <a v-bind:href="icon.url" target="_blank" rel="noopener noreferrer"><img v-bind:src="icon.img" alt="Icon" srcset=""><p>{{icon.name}}</p></a>
</template>

<script>
export default {
  name: 'AboutIcon',
  props: {
    icon: {
      required: true,
    }
  },
}
</script>

<style scoped>
a {
	display: flex;
	flex-direction: column;
	justify-content: center;
	text-align: center;
	transition: .3;
	margin: 5px;
}
a:hover img {
  opacity: .5;
}
img {
  height: 56px;
  transition: opacity 0.3s;
}

@media only screen and (max-width: 767px) {

}
</style>
