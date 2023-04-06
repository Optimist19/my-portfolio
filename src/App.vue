<template>
  <div class="header">
    <h1>{{myPortfolio}}</h1>
    <div class="a-con">
      <a href="#home">{{home}}</a>
      <a href="#about">{{aboutMe}}</a>
      <a href="#project">{{projects}}</a>
    </div>
  </div>
  <AboutView id="home" />
  <ProjectsView id="about" />
  <HomeView id="project" />
</template>

<script>
import {ref} from "vue"
import HomeView from './components/HomeView.vue'
import AboutView from './components/AboutView.vue'
import ProjectsView from './components/ProjectsView.vue'

export default {
  name: 'App',
  components: {
    HomeView,
    AboutView,
    ProjectsView
  },
  setup(){
    const myPortfolio = ref("My Portfolio")
    const home = ref("Home")
    const aboutMe = ref("About")
    const projects = ref("Project")


    return{
      myPortfolio,
      home,
      aboutMe,
      projects
    }
  }
}
</script>

<style>
html {
  scroll-behavior: smooth;
}

.header{
  height: 10vh;
  position: fixed;
  top: 0;
  /* left: -100%; */
  background-color: blueviolet;
  width: 100%;
  display: flex;

  justify-content: space-around;
  align-items: center;

}

h1{

  color: rgb(250, 249, 246);
}

.a-con{

}
a{
  color: rgb(250, 249, 246);
  text-decoration: none;
  margin-right: 2vw;
}
/* #app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
} */
</style>
