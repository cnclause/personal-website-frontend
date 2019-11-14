
<template>
  <div id="app">
    <router-view/>
  </div>
</template>

<style lang="scss">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: white;
  // background: #DCC7AA;
  // background: #6B7A8F;
}




#nav {
  padding: 10px;

  a {
    font-weight: bold;
    color: 	white;
    font-size: 20pt;

    &.router-link-exact-active {
      color: #DCC7AA;
    }
  }
}
  

  

</style>
