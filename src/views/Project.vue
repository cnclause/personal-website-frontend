<template>
  <div class="projects">
    <h1> projects </h1>
    <div class="nav">
          <router-link to="/">Home</router-link> 
          <router-link to="/projects">Projects</router-link>
          <router-link to="/resume">Resume</router-link>
          <router-link to="/contact">Contact</router-link> 
    </div>
    <ProjectContainer />
  </div>
</template>

<script>

import ProjectContainer from '@/components/ProjectContainer.vue'

export default {
  name: 'projects',
  components: {
    ProjectContainer
  }

}

</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css?family=Raleway&display=swap');
@import url('https://fonts.googleapis.com/css?family=Montserrat&display=swap');
@import url('https://fonts.googleapis.com/css?family=Lora&display=swap');


h1{
  font-size: 50pt;
  margin-top: 0;
  padding-top: 2rem;
  font-family: 'Lora', serif;

}


  
.nav {
  display: flex;
  justify-content: space-evenly;
  color: black;
  margin-top: 5rem;
  margin-bottom: 5rem;
  padding: 10px;
  font-family: 'Raleway', sans-serif;
  text-transform: uppercase;
 

  a {
    text-decoration: none;
    text-align: center;

    font-weight: bold;
    color: 	#1955Fa;
    font-size: 15pt;

    &.router-link-exact-active {
      color: #38C3FF;
    }
  }
}

.projects {
  font-family: 'Montserrat', sans-serif;
}

</style>


