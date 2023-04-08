<template>
	<div class="container">
		<p class="title">{{title}}</p>
		<div class="con">
			<div v-for="project in projects" :key="project.id" class="project-con">
				<a :href="project.link" target="_blank">
					<div v-if="show">
						<i class="fa-solid fa-rotate fa-spin"></i>
					</div>
					<div v-else>
						<img :src="project.img" alt="project-thumbnail" />
					</div>
					<p>
						Name: {{project.name}}
					</p>
					<a :href="project.github" target="_blank"><button>Github-repo</button></a>
					
					<p>
						Project-Des: {{ project.description }}
					</p>
				</a>
			</div>
		</div>
	</div>
</template>

<script>
import data from "../../projects.json"
import {ref} from "vue"
export default {
	name: "ProjectsView",
	setup(){
		const projects = ref(data)
		const title = ref("Project")
		const show = ref(true)
		setTimeout(() =>{
			show.value = false
		},2000)

		console.log(projects)


		return{
			projects,
			title,
			show
		}

	}
}
</script>

<style scoped>

.title{
	padding-top: 4vh;
	padding-bottom: 4vh;
	text-align: center;
	color: green;
	font-family: 'Montserrat Alternates', sans-serif;
	font-weight: bold;
	font-size: 20px;
}
.con{
	display: flex;
	flex-wrap: wrap;
	font-family: 'Lato', sans-serif;
	gap: 4vh 0;
}

.project-con{
	max-width: 40vw;
	margin: 0 auto;
}

.project-con p{
	margin-top: 1vh;
}

img{
	max-width: 40vw;
}

a{
	color: rgb(250, 249, 246);
	text-decoration: none;
}

button{
	margin-top: 5px;
	cursor: pointer;
	background-color: green;
	border: none;
	padding: 2px 2px;
	border-radius:  2px;
}

@media only screen and (max-width: 574px) {
	.con{
		display: block;
	}

	.project-con{
		max-width: 80vw;
	}

	img{
		max-width: 80vw;

	}

	.title{
		font-size: 18px;
	}
}


@media only screen and (max-width: 375px) {
	.title{
		font-size: 16px;
	}
}


</style>