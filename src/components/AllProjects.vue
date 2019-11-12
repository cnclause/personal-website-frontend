<template>
<div class = 'projects'>
    <h1> Projects HUR </h1>
    <div :key='project.id' v-for="project in projects">
        <h2 > {{project.title}} </h2>
        <p> {{project.description}} </p>
        <img :src='project.image_url'/>
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