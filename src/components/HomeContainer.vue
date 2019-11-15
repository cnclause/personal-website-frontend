<template>
    <div class="home-container" >
       <header>
            <!-- <img src='../images/hikingpng.png' alt="hikingpic" /> -->
            <div class="title-and-links">
                <h1 class = "title"> Cat Clause </h1>
                  <div id="nav">
                  <router-link to="/projects">Projects</router-link>
                  <router-link to="/resume">Resume</router-link>
                  <router-link to="/contact">Contact</router-link> 
                </div>
                  <a
                    href="https://github.com/cnclause"
                    class="icon git-icon"
                    target="_blank"
                    rel="noopener noreferrer"
                  >
                      <img src='../images/bluegit.png' alt="github"/> 
                  </a>
                  <a
                    href="https://medium.com/@cnclause123"
                    class="icon medium-icon"
                    target="_blank"
                    rel="noopener noreferrer"
                  >
                    <img src='../images/blueblog.png' alt="medium"/> 
                  </a>
                  <a
                    href="https://www.linkedin.com/in/catherine-clause-a15b58191/"
                    class="icon linkedin-icon"
                    target="_blank"
                    rel="noopener noreferrer"
                  >
                    <img src='../images/bluelinkedin.png' alt="linkedin"/>
                  </a>
              
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
  padding-right: 15rem;
}



.title {
    font-size: 55pt;
    font-family: 'Lora', serif;
    font-weight: bold;
    color: white;
    width: 400px;
    text-align: center;

  }

#nav {
  display: flex;
  justify-content: space-evenly;
  color: black;
  padding: 0;
  padding-top: 1rem;
  width: 100%;
  font-family: 'Raleway', sans-serif;
  text-transform: uppercase;


  a {
    text-decoration: none;
    text-align: center;

    font-weight: bold;
    color: 	white;
    font-size: 15pt;
    text-shadow: 1px 1px 1px black;

    &.router-link-exact-active {
      color: #38C3FF;
    }
  }
}


.icon {
    cursor: pointer;
    padding: 1rem;
  }

img {
  width: 4rem;
  padding-top: 1rem;
  padding-bottom: 1rem;
}




</style>