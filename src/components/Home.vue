<template>
	<section>
		<h2> {{this.greeting}}</h2>
		<h4> {{this.introMessageTyped}} <span>|</span> </h4>
		<small> Front end development / UI and UX-Designer </small>
		<div class="social-container">
			<a href="https://github.com/Mumis" target="_blank" rel="noopener noreferrer"><i class="fab fa-github"></i></a>
			<a href="https://www.linkedin.com/in/emilwertwein/" target="_blank" rel="noopener noreferrer"><i class="fab fa-linkedin-in"></i></a>
			<a href="https://twitter.com/wertwein" target="_blank" rel="noopener noreferrer"><i class="fab fa-twitter"></i></a>	
		</div>
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
				{ id: 8, text: "Hej Hej!" },
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
					this.greeting = this.greetingList[Math.floor(Math.random() * this.greetingList.length)].text;
				}
			}
			else if (hour >= 12 && hour <= 17) {
				if (Math.random() * 3 < 2) {
					this.greeting = this.greetingHourly.afternoon;
				}
				else {
					this.greeting = this.greetingList[Math.floor(Math.random() * this.greetingList.length)].text;
				}
			} else {
				if (Math.random() * 3 < 2) {
					this.greeting = this.greetingHourly.evening;
				}
				else {
					this.greeting = this.greetingList[Math.floor(Math.random() * this.greetingList.length)].text;
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

@keyframes fadeIn {
0% { opacity: 0}
100% { opacity: 1}
}

@keyframes scroll {
	0% {
		opacity: 1;
		transform: translateY(0);
	}
	100% {
		opacity: 0;
		transform: translateY(15px);
	}
}
section {
	display: flex;
	flex-direction: column;
	justify-content: center;
	align-items: center;
	text-align: center;
	height: 100vh;
	background-color: rgb(255, 218, 208);
	transform: skewY(2deg);
	transform-origin: top right;
	box-shadow: inset 0px -25px 25px -25px rgba(0,0,0,0.50);
	outline: 1px solid transparent;
	padding: 0 5px;
}
section > * {
	transform: skewY(-2deg);
	animation: fadeIn;
	animation-duration: 2s;
}
span {
	animation: blink;
	animation-duration: 0.9s;
	animation-iteration-count: infinite;
	animation-timing-function: linear;
	animation-delay: 2.7s;
}
h2 {
	margin-bottom: 20px;
}
.mouse {
	position: absolute;
	bottom: 50px;
	width: 28px;
	height: 48px;
	border-radius: 11px 11px 15px 15px;
	border: 1px solid #4A2A18;
	transition: opacity .4s;
}
.mouse > span {
	display: block;
	margin: 6px auto;
	width: 2px;
	height: 5px;
	border-radius: 4px;
	background: #4A2A18;
	border: 1px solid transparent;
	animation: scroll;
	animation-duration: 1s;
	animation-iteration-count: infinite;
	animation-timing-function: linear;
}
.social-container {
	margin-top: 50px;
}
.social-container i {
	margin: 0 30px;
	font-size: 25px;
	transition: color .2s;
}
.social-container i:hover {
	color: #B2704E;
}
</style>
