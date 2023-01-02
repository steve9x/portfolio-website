<template>
  Hello from the app Component
  <HelloWorld />
</template>

<script>
import HelloWorld from './components/About.vue'
import './app.css'

export default {
  name: 'App',
  components: {
    HelloWorld
  }
}
</script>
