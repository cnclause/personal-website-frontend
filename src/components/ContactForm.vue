<template>
<div class="contact-form-container">
    <form v-on:submit.prevent="submitContact($event)" id='contactForm' class='contact-form'>
        <p>
            <label>Name</label>
             <input type="name" name="name" placeholder="Name" >
        </p>
        <p>
            <label>Email Address</label>
            <input type="email" name="email" placeholder="example@email.com" >
        </p>
        <p>
            <label>Phone Number</label>
             <small>Format: 123-456-7890</small>
            <input type="tel" name="phone"
                pattern="[0-9]{3}-[0-9]{3}-[0-9]{4}"
                placeholder="123-456-7890"
                required
            >
           
        </p>
        <p class="full">
            <label>Message</label>
            <textarea name="message" rows="5"></textarea>
        </p>
        <p class="full">
            <button type="submit">Send Email</button>
        </p>
        <output>

        </output>
    </form>
</div>
</template>

<script>


export default { 
    name: 'ContactForm',
    methods: {
        submitContact(event){
            const formData = new FormData(event.target)
            const name = formData.get("name")
            const email = formData.get("email")
            const phone = formData.get("phone")
            const message = formData.get("message")
          
            fetch('https://personal-website-cat.herokuapp.com/send', {
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

@import url('https://fonts.googleapis.com/css?family=Raleway&display=swap');
@import url('https://fonts.googleapis.com/css?family=Montserrat&display=swap');

    

    .contact-form-container {
        width: 100%;
        justify-content: center;
        font-family: 'Montserrat', sans-serif;
        
    }

    .contact-form-container input, label{
        display: flex;
        justify-items: center;
        width: 25rem;
        height: 2rem;
    }

    label{
        align-items: center;
        justify-content: center;
    }

    .contact-form {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: space-evenly;
        height: 30rem;
    }

    .contact-form textarea{
        width: 25rem;
        height: 3rem;
        font-size: 11pt;
    }

    button {
        width: 10rem;
        height: 2rem;
        font-size: 11pt;
    }

    input {
        font-size: 11pt;
    }

    small{
        color:lightslategray;
    }

</style>