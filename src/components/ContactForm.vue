<template>
<div class="contact-form-container">
        <h1> Contact Me </h1>
    <form class='contact-form'>
        <p>
            <label>Name</label>
            <input type="text" name="name">
        </p>
        <p>
            <label>Email Address</label>
            <input type="email" name="email">
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
    </form>
</div>
</template>

<script>
export default { 
    name: 'ContactForm',
    props: {
        msg: String
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