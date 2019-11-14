<template>
  <div class="projects">
    <div class="nav">
          <router-link to="/">About Me</router-link> 
          <router-link to="/projects">Projects</router-link>
          <router-link to="/resume">Resume</router-link>
          <router-link to="/contact">Contact</router-link> 
    </div>
    <!-- <h1>Projects</h1> -->
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

<style scoped lang="scss">
@import url('https://fonts.googleapis.com/css?family=Raleway&display=swap');
@import url('https://fonts.googleapis.com/css?family=Montserrat&display=swap');

h1{
  // color: #F7C331;
  font-size: 40pt;
  margin-top: 0;
  padding-top: 2rem;

}


  
.nav {
  display: flex;
  justify-content: space-evenly;
  color: black;
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


