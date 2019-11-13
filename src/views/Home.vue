<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <HomeContainer />
  </div>
</template>

<script>
// @ is an alias to /src
import HomeContainer from '@/components/HomeContainer.vue'

export default {
  name: 'home',
  components: {
    HomeContainer
  }
}
</script>


