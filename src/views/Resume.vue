<template>
    <div class="resume-page">
        <h1 id="resume-title"> resume </h1>
        <div class="nav">
          <router-link to="/">Home</router-link> 
          <router-link to="/projects">Projects</router-link>
          <router-link to="/resume">Resume</router-link>
          <router-link to="/contact">Contact</router-link> 
        </div>
        <button @click="onClick()">
            Download Resume
        </button>
        <ResumeContainer />
    </div>

</template>

<script>

import ResumeContainer from '@/components/ResumeContainer.vue'
import Vue from 'vue'
import axios from 'axios'
import VueAxios from 'vue-axios'
 
Vue.use(VueAxios, axios)

export default {
    name: 'resume',
    components: {
        ResumeContainer
    },
    methods: {
    onClick() {
        axios({
            url: 'https://personal-website-cat.herokuapp.com/downloadFile',
            method: 'GET',
            responseType: 'blob',
        }).then((response) => {
                var fileURL = window.URL.createObjectURL(new Blob([response.data]));
                var fileLink = document.createElement('a');

                fileLink.href = fileURL;
                fileLink.setAttribute('download', 'file.pdf');
                document.body.appendChild(fileLink);

                fileLink.click();
        });
    }

    }
}

</script>

<style scoped lang="scss">
@import url('https://fonts.googleapis.com/css?family=Raleway&display=swap');
@import url('https://fonts.googleapis.com/css?family=Montserrat&display=swap');
@import url('https://fonts.googleapis.com/css?family=Lora&display=swap');


#resume-title{
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
    cursor: pointer;

    &.router-link-exact-active {
      color: #38C3FF;
    }
  }
}

.resume-page {
  font-family: 'Montserrat', sans-serif;
}

button {
    font-family: 'Montserrat', sans-serif;
    width: 15rem;
    height: 3rem;
    font-size: 15pt;
    border: none;
    box-shadow: 0 4px 4px 0 rgba(0,0,0,0.2), 0 3px 4px 0 rgba(0,0,0,0.19);
    border-radius: 3px;
    color: 	#1955Fa;
    font-weight: bold;
    cursor: pointer;
    transition: transform 0.5s;
}

button:hover {
    transform: scale(0.95)
}



</style>