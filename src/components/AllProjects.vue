<template>
<div class = 'projects'>
    <h1> Projects HUR </h1>
    <h3> {{projects}} </h3>
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