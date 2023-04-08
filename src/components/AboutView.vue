<template>
  <div class="con">
	<div class="p">
		<!-- <img src="../assets/IMG_2022.jpg" alt="profile-pic" /> -->
		<p>
			I am a Frontend Developer looking forward to getting employed as an Intern. Where I can get to showcase the basic skills, experience, and passion for frontend development also contribute to your company's success and in the process get to hone my skills as Frontend Developer.
		</p>
		<p>
			I have experience working with some number of programming languages, frameworks, and tools, including HTML, CSS, JavaScript, Vue.js, Git, Github, Slack, Netlify. I am also an excellent communicator and collaborator.
		</p>
		<p>
			I will be excited about the opportunity to join your company as an intern and I am confident to contribute to the growth and development of your company. 
		</p>
	</div>
  </div>
</template>

<script>
export default {
  name: "AboutView",
};
</script>

<style scoped>
.con {
	margin-top: 10vh;
	color: rgb(250, 249, 246);
}

h2{
	text-align: center;
}

.p{
	margin-top: 7vh;
	margin-left: 5vw;
	margin-right: 5vw;
	font-family: 'Lato', sans-serif;
	font-size: 20px;
}

p{
	text-align: left;
}

/* img{
	float: right;
	max-width: 15vw;
	border-radius: 50%;
} */


@media only screen and (max-width: 574px) {
	.p{
		font-size: 18px;
	}
}

@media only screen and (max-width: 375px) {
	.p{
		font-size: 16px;
	}
}

</style>
