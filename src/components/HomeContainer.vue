<template>
    <div class="home-container" >
       <header>
            <img src='../images/hikingpng.png' alt="hikingpic" />
            <h1 class = "title"> Hey, I'm Cat </h1>
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


.title {
    font-size: 40pt;
  }

img {
    width: 45rem;
    border-radius: 5px;
  }

</style>