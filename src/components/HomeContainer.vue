<template>
    <div class="home-container" >
        <h1> {{msg}} </h1>
        <AllProjects 
            :projects = "projects"
        />
        <ContactForm />
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
        AllProjects,
        ContactForm
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
        }
    }
}

</script>

<style scoped lang="scss">

.home-container{
    display: flex;
    justify-content: space-between;
}

h1 {
   color: blue;
}

</style>