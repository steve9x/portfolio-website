<template>
  <Header />
  <RouterView />
</template>

<script>

import Header from './components/Header.vue'
import './app.css'

export default {
  name: 'App',
  components: {
    Header
  }
}
</script>
