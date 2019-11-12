<template>
    <div class="home-container" >
        <h1> {{msg}} </h1>
        <ContactForm msg ="Contact Me"/>
        <AllProjects 
            :projects = "projects"
        />
    </div>

</template>


<script>
import ContactForm from './ContactForm.vue'
import AllProjects from './AllProjects.vue'


export default {
    name: 'HomeContainer',
    props: {
        msg: String
    },
    components: {
        ContactForm,
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
            fetch('http://localhost:3000/api/projects')
                .then(response => response.json())
                .then(projects => {this.projects = projects})
        },

        mapProjects(){
            let projects = this.projects
            return projects.map(project => {
                return project.title
            })
        }   
    }
}

</script>

<style scoped lang="scss">

h1 {
   color: blue;
}

</style>