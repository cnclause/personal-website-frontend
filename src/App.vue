
<template>
  <div id="app">
    <div id="nav">
        <router-link to="/">About Me</router-link> |
        <router-link to="/projects">Projects</router-link> |
        <router-link to="/resume">Resume</router-link> |
    </div>
    <router-view/>
  </div>
</template>

<style lang="scss">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #DCC7AA;
  // background: #DCC7AA;
  background: #6B7A8F;
}




#nav {
  padding: 10px;

  a {
    font-weight: bold;
    color: 	#F7882F;
    font-size: 20pt;

    &.router-link-exact-active {
      color: #DCC7AA;
    }
  }
}
  

  

</style>
