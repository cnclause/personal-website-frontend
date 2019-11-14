<template>
    <div class="home-container" >
       <header>
            <!-- <img src='../images/hikingpng.png' alt="hikingpic" /> -->
            <div class="title-and-links">
                <h1 class = "title"> Cat Clause </h1>
                <img src='../images/bluegit.png' alt="github"/> 
                <img src='../images/blueblog.png' alt="medium"/> 
                <img src='../images/bluelinkedin.png' alt="linkedin"/> 
              <div id="nav">
                <router-link to="/projects">Projects</router-link>
                <router-link to="/resume">Resume</router-link>
                <router-link to="/contact">Contact</router-link> 
              </div>
            </div>
        </header>
     <router-view/>
    </div>
</template>



<style scoped lang="scss">

// @import url('https://fonts.googleapis.com/css?family=Julius+Sans+One&display=swap');
@import url('https://fonts.googleapis.com/css?family=Lora&display=swap');
@import url('https://fonts.googleapis.com/css?family=Raleway&display=swap');

.home-container{
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    background-image: url('../images/hikingpng.png');
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center;
    // width:100%;
    height: 70rem;
}

header {
  display: flex;
  justify-content: flex-end;
  padding-bottom: 5rem;
  padding-top: 20rem;
}

.title-and-links {
  width: 20%;
  padding-right: 15rem;
}


.title-and-links img{
  width: 4rem;
  margin: 1rem;
}


.title {
    font-size: 50pt;
    font-family: 'Lora', serif;
    font-weight: bold;
    color: white;
  }

#nav {
  display: flex;
  justify-content: space-around;
  color: black;
  padding: 10px;
  width: 100%;
  font-family: 'Raleway', sans-serif;
  text-transform: uppercase;

  a {
    text-decoration: none;
    text-align: center;

    font-weight: bold;
    color: 	white;
    font-size: 15pt;

    &.router-link-exact-active {
      color: #38C3FF;
    }
  }
  
}

img {
    width: 45rem;
    border-radius: 5px;
  }



</style>