<template>
<div class="contact-form-container">
        <h1> Contact Me </h1>
    <form v-on:submit.prevent="submitContact($event)" id='contactForm' class='contact-form'>
        <p>
            <label>Name</label>
            <input type="text" v-model="text" name="name">
        </p>
        <p>
            <label>Email Address</label>
            <input type="email" name="email" >
        </p>
        <p>
            <label>Phone Number</label>
            <input type="text" name="phone">
        </p>
        <p class="full">
            <label>Message</label>
            <textarea name="message" rows="5"></textarea>
        </p>
        <p class="full">
            <button type="submit">Submit</button>
        </p>
        <output>

        </output>
    </form>
</div>
</template>

<script>
export default { 
    name: 'ContactForm',
    data(){
        return {
            text: ''
        }
    },
    methods: {
        submitContact(event){
            const formData = new FormData(event.target)
            const name = formData.get("name")
            const email = formData.get("email")
            const phone = formData.get("phone")
            const message = formData.get("message")
          
            fetch('http://localhost:3000/send', {
                method: 'POST',
                headers: {'Content-Type':'application/json'},
                body: JSON.stringify({ name, email, phone, message})
                })
            event.target.reset()
            }
        }
}

</script>

<style scoped lang="scss">

    .contact-form-container {
        padding-right: 5rem;
    }

    .contact-form-container input, label {
        display: flex;
        justify-items: center;
    }

    .contact-form {
        display: flex;
        flex-direction: column;
        align-items: center;
    }

</style>