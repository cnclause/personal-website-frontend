<template>
<div class="projects" >
    <div  class='projects-container'>
        <div :key='project.id' v-for="project in projects" class='projects-card'>
            <img :src='project.image_url' class="project-image"/>
            <div class="project-info">
                <h2 > {{project.title}} </h2>
                <p> {{project.description}} </p>
                <h4> {{project.technologies}}</h4>
                <a :href='project.deployment_link'> Deployment Link </a>
            </div>
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
    width: 100%
} 

.projects-card {
    display: flex;
    flex-direction: column;
    align-items:center;
    margin-top: 2rem;
    width: 60%;
}

.project-info{
    display: flex;
    flex-direction: column;
    width: 50%;
    padding: 5rem;
}

.project-info p, a{
    padding: 1rem;
}

.project-info p{
    padding: 1rem;
    line-height: 30px;
}

.project-image{
    width: 100%;
    // border-radius: 8px;
}

h4{
    font-style: italic;
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