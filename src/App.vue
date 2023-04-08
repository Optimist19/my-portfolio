<template>
  <div class="header">
    <h1>{{myPortfolio}}</h1>
    <div class="a-con">
      <a href="#about">{{aboutMe}}</a>
      <a href="#project">{{projects}}</a>
      <a href="#contact">{{contact}}</a>
    </div>
  </div>
  <AboutView id="about" />
  <ProjectsView id="project" />
  <ContactView id="contact" />
</template>

<script>
import {ref} from "vue"
import ContactView from './components/ContactView.vue'
import AboutView from './components/AboutView.vue'
import ProjectsView from './components/ProjectsView.vue'

export default {
  name: 'App',
  components: {
    ContactView,
    AboutView,
    ProjectsView
  },
  setup(){
    const myPortfolio = ref("My Portfolio")
    const contact = ref("Contact")
    const aboutMe = ref("About")
    const projects = ref("Project")


    return{
      myPortfolio,
      contact,
      aboutMe,
      projects
    }
  }
}
</script>

<style scoped>
html {
  scroll-behavior: smooth;
}

.header{
  height: 10vh;
  position: fixed;
  top: 0;
  width: 100%;
  display: flex;
  justify-content: space-around;
  align-items: center;

}

h1{
  font-family: 'Lato', sans-serif;
  color: green;
}

a{
  color: green;
  text-decoration: none;
  margin-right: 2vw;
  font-family: 'Montserrat Alternates', sans-serif;
  font-weight: bold;
	font-size: 22px;
}

@media only screen and (max-width: 574px) {
  h1{
    font-size: 18px;
  }

  a{
    font-size: 18px;
  }

}

@media only screen and (max-width: 375px) {
  h1{
    font-size: 14px;
  }

  a{
    font-size: 14px;
  }
}

</style>
