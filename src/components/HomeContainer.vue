<template>
    <div class="home-container" >
       <header>
            <img src='../images/hikingpng.png' alt="hikingpic" />
            <div class="title-and-links">
              <h1 class = "title"> Hey, I'm Cat </h1>
              <img src='../images/github.png' alt="github"/> 
              <img src='../images/medium.png' alt="medium"/> 
              <img src='../images/linkedin.png' alt="linkedin"/> 
            </div>
        </header>
     <router-view/>

        <ContactForm />
    </div>

</template>


<script>
import ContactForm from './ContactForm.vue'

export default {
    name: 'HomeContainer',
    components: {
        ContactForm
    }
}

</script>

<style scoped lang="scss">

.home-container{
    display: flex;
    flex-direction: column;
    justify-content: space-between;
}

header {
  display: flex;
  justify-content: space-evenly;
  padding-bottom: 5rem;
}



.title-and-links img{
  width: 3rem;
  margin: 1rem;
}


.title {
    font-size: 40pt;
  }

img {
    width: 45rem;
    border-radius: 5px;
  }



</style>