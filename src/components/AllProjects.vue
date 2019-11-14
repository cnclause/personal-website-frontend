<template>
<div class="projects" >
    <div  class='projects-container'>
        <div :key='project.id' v-for="project in projects" class='projects-card'>
            <h2 > {{project.title}} </h2>
            <img :src='project.image_url' class="project-image"/>
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

.projects-container {
    display: flex;
    justify-content: center;
} 

.projects-card {
    margin-top: 2rem;
    width: 33%;
}

.project-image{
    width: 75%;
    border-radius: 8px;
}

h2 {
    color: #F7882F;
    font-size: 25pt;
    text-shadow: 1px 1px #323944;
}



</style>