<template>
	<section>
		<h2> {{this.message}}</h2>
	</section>
</template>

<script>
export default {
	name: 'Home',
	data: function() {
		return {
			messageRandom: [
				{ id: 1, text: "Hello," },
				{ id: 2, text: "Hello there," },
				{ id: 3, text: "Howdy!" },
				{ id: 4, text: "Good to see you," },
				{ id: 5, text: "Nice to meet you!" },
				{ id: 6, text: "Aloha!" },
				{ id: 7, text: "Greetings!" },
			],
			messagePerHour: {
				morning: "Good Morning,",
				afternoon: "Good Afternoon,",
				evening: "Good Evening," 
			}
			,
			message: "",
		}
	},
	methods: {
		chooseMessage: function() {
			const now = new Date();
			const hour = now.getHours();
			if (hour < 12) {
				if (Math.random() * 3 < 2) {
					this.message = this.messagePerHour.morning;
				}
				else {
					this.message = this.messageRandom[Math.round(Math.random() * this.messageRandom.length - 1)].text;
				}
			}
			else if (hour >= 12 && hour <= 17) {
				if (Math.random() * 3 < 2) {
					this.message = this.messagePerHour.afternoon;
				}
				else {
					this.message = this.messageRandom[Math.round(Math.random() * this.messageRandom.length - 1)].text;
				}
			} else {
				if (Math.random() * 3 < 2) {
					this.message = this.messagePerHour.evening;
				}
				else {
					this.message = this.messageRandom[Math.round(Math.random() * this.messageRandom.length - 1)].text;
				}
			}
		},
	},
	created() {
		this.chooseMessage();
	},
}
</script>

<style>
	section {
		display: flex;
		justify-content: center;
		align-items: center;
		height: 100vh;
		background-color: rgb(255, 218, 208);
	}
</style>
