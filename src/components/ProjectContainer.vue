<template>
    <div class="project-container" >
        
        <AllProjects 
            :projects = "projects"
        />
    </div>

</template>

<script>
import AllProjects from './AllProjects.vue'

export default {
    name: 'ProjectContainer',
    components: {
        AllProjects
    },
    data(){
        return {
            projects: []
      }
    },
    mounted(){
        this.getAllProjects()
    },
    methods: {
        getAllProjects(){
            fetch('http://personal-website-cat.herokuapp.com/api/projects')
                .then(response => response.json())
                .then(projects => {this.projects = projects})
        }
    }
}

</script>

<style>




</style>


