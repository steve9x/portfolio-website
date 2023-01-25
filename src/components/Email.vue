<template>
  <div class="form-wrapper">
    <form class="input-form">
      <label>Name</label>
      <input type="text" v-model="formData.name" required>
      <label>Email</label>
      <input type="email" v-model="formData.email" required>
      <label>Message</label>
      <textarea v-model="formData.message" ></textarea>
      <button @submit.prevent="sendEmail">Send</button>
    </form>
  </div>
</template>

<script>
// import emailjs from '@emailjs/browser';
import{ ref } from 'vue'
export default {
  setup () {
    const formData = ref({
      name: '',
      email: '',
      message: ''
    })

    const sendEmail = () => {
      // Sende E-mail here!!!

      // clean Form
      formData.value = {
        name: '',
        email: '',
        message: ''
      }
    }
    return {
      formData,
      sendEmail
    }
  }
  // methods: {
    // sendEmail() {
    //   emailjs.sendForm('YOUR_SERVICE_ID', 'YOUR_TEMPLATE_ID', form, 'YOUR_PUBLIC_KEY')
    //     .then((result) => {
    //       console.log('SUCCESS!', result.text);
    //     }, (error) => {
    //       console.log('FAILED...', error.text);
    //     });
    // }
  // }
}
</script>
