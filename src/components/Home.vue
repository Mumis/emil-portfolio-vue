<template>
	<section>
		<h2> {{this.greeting}}</h2>
		<h4> {{this.introMessageTyped}} <span>|</span> </h4>
		<small> Front end development / UI and UX-Designer </small>	
		<div class="mouse">
			<span> </span>
		</div>
	</section>
</template>

<script>
export default {
	name: 'Home',
	data: function() {
		return {
			greetingList: [
				{ id: 1, text: "Hello," },
				{ id: 2, text: "Hello there," },
				{ id: 3, text: "Howdy!" },
				{ id: 4, text: "Good to see you," },
				{ id: 5, text: "Nice to meet you!" },
				{ id: 6, text: "Aloha!" },
				{ id: 7, text: "Greetings!" },
			],
			greetingHourly: {
				morning: "Good Morning,",
				afternoon: "Good Afternoon,",
				evening: "Good Evening," 
			},
			greeting: "",
			introMessage: "I'm Emil, a web developer.",
			introMessageTyped: "",
		}
	},
	methods: {
		chooseMessage: function() {
			const now = new Date();
			const hour = now.getHours();
			if (hour < 12) {
				if (Math.random() * 3 < 2) {
					this.greeting = this.greetingHourly.morning;
				}
				else {
					this.greeting = this.greetingList[Math.round(Math.random() * this.greetingList.length - 1)].text;
				}
			}
			else if (hour >= 12 && hour <= 17) {
				if (Math.random() * 3 < 2) {
					this.greeting = this.greetingHourly.afternoon;
				}
				else {
					this.greeting = this.greetingList[Math.round(Math.random() * this.greetingList.length - 1)].text;
				}
			} else {
				if (Math.random() * 3 < 2) {
					this.greeting = this.greetingHourly.evening;
				}
				else {
					this.greeting = this.greetingList[Math.round(Math.random() * this.greetingList.length - 1)].text;
				}
			}
		},
		startTypeIntro: function() {
			for (let i in this.introMessage) {
					setTimeout(() => {
							this.introMessageTyped = this.introMessageTyped + this.introMessage[i];
					}, 130*i);
			}
		}
	},
	created() {
		this.chooseMessage();
		this.startTypeIntro();
	},
}
</script>

<style scoped>
	@keyframes blink {
    0% { opacity: 1; }
    49% { opacity: 1; }
    50% { opacity: 0; }
    100% { opacity: 0; }
	}

	span {
		animation: blink;
		animation-duration: 0.9s;
    animation-iteration-count: infinite;
    animation-timing-function: linear;
    animation-delay: 2.7s;
	}

	section {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		text-align: center;
		height: 100vh;
		padding: 0 4px;
		background-color: rgb(255, 218, 208);
	}

	h2 {
		margin-bottom: 15px;
	}
</style>
