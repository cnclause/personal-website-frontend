<template>
    <div class="home-container" >
       <header>
            <!-- <img src='../images/hikingpng.png' alt="hikingpic" /> -->
            <div class="title-and-links">
                <h1 class = "title"> Cat Clause </h1>
                <img src='../images/github.png' alt="github"/> 
                <img src='../images/medium.png' alt="medium"/> 
                <img src='../images/linkedin.png' alt="linkedin"/> 
              <div id="nav">
                <router-link to="/">About Me</router-link> |
                <router-link to="/projects">Projects</router-link> |
                <router-link to="/resume">Resume</router-link> |
                <router-link to="/contact">Contact</router-link> 
              </div>
            </div>
        </header>
     <router-view/>
    </div>
</template>



<style scoped lang="scss">

@import url('https://fonts.googleapis.com/css?family=Julius+Sans+One&display=swap');

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
  padding-right: 15rem;
}


.title-and-links img{
  width: 3rem;
  margin: 1rem;
}


.title {
    font-size: 40pt;
    font-family: 'Julius Sans One', sans-serif;
    font-weight: bold;
    color: white;
  }

img {
    width: 45rem;
    border-radius: 5px;
  }



</style>