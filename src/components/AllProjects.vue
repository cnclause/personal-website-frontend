<template>
<div class="projects" >
     <h1> Projects HUR </h1>
    <div  class='projects-container'>
        <div :key='project.id' v-for="project in projects" class='projects-card'>
            <h2 > {{project.title}} </h2>
            <img :src='project.image_url'/>
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
} 

.projects-card {
    width: 50%;
}

.projects-card img {
    width: 75%;
}



</style>