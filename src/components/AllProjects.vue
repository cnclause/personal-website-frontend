<template>
<div class="projects" >
    <div  class='projects-container'>
        <div :key='project.id' v-for="project in projects" class='projects-card'>
            <img :src='project.image_url' class="project-image"/>
            <h2 > {{project.title}} </h2>
            <p> {{project.description}} </p>
            <a :href='project.deployment_link'> Deployment Link </a>
        </div>
    </div>
</div>
</template>


<script>
export default {
    name: 'AllProjects',
    props: {
        projects: Array
    }      

}
</script>

<style scoped lang="scss">

.projects{
    display: flex;
    justify-content: center;
}

.projects-container {
    display: flex;
    flex-direction: column;
    align-items: center;
    width: 80%
} 

.projects-card {
    margin-top: 2rem;
    width: 90%;
}

.project-image{
    width: 75%;
    border-radius: 8px;
}

h2 {
    color: #1955Fa;
    font-size: 25pt;
}

a{
    text-decoration: none;
    color: #38C3FF;
}



</style>