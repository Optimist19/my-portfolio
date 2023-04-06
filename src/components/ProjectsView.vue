<template>
	<div>
		<p>ProjectsView</p>
		<div v-for="api in newData" :key="api">
			<p>{{ api.name }}</p>
			<!-- <p>{{ api.url. }}</p> -->
			<a :href="`${api.url.value}` "> click</a>
			<p>{{ api.html_url }}</p>
			<!-- <p>{{ api.url }}</p> -->
			<div v-for="repo in api.owner" :key="repo.id">
				{{ repo.id }}
			</div>

		</div>
	</div>
</template>

<script>
import {onMounted, ref} from "vue"
export default {
	name: "ProjectsView",
	setup(){

		let newData = ref([])
		// let url = ref("https://zippy-marzipan-7ed47e.netlify.app/")
		let data = ref(null)
		console.log(data)
		onMounted(() =>{
			// out()
		})

		async function out(){
    await fetch('https://api.github.com/users/Optimist19/repos')
    .then(res => res.json())
    .then(result => data.value = result)
	for(let i = 0; i < data.value.length; i++){
		// if(i === 28 && i === 5){
		// 	newData.value.push(data.value[i])
		// }

		
		switch(i){
			case 5:
			newData.value.push(data.value[i],{url: "https://zippy-marzipan-7ed47e.netlify.app/"})
			continue;
			case 18:
			newData.value.push(data.value[i])
			continue;
			case 19:
			newData.value.push(data.value[i])
			continue;
			case 21:
			newData.value.push(data.value[i])
			continue;
			case 22:
			newData.value.push(data.value[i])
			continue;
			case 27:
			newData.value.push(data.value[i])
			continue;
			case 28:
			newData.value.push(data.value[i])
			break;
			default:
				console.log("You are doing well")
		}
	}
	}
	console.log(newData.value)


	return{
		data,
		out,
		newData,
		// url
	}

	}
}
</script>

<style scoped>
div{
	height: 60vh;
	background-color: black;
}
</style>