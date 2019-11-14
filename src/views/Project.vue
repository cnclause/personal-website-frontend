<template>
  <div class="projects">
    <h1>Projects</h1>
    <ProjectContainer />
  </div>
</template>

<script>

import ProjectContainer from '@/components/ProjectContainer.vue'

export default {
  name: 'projects',
  components: {
    ProjectContainer
  }

}

</script>

<style scoped lang="scss">

h1{
  // color: #F7C331;
  font-size: 40pt;
  margin-top: 0;
  padding-top: 2rem;

}

.projects {
  background-color: #6B7A8F;
  color: #DCC7AA;
}

</style>


