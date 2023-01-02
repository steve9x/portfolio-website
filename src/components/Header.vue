<template>
  <nav class="navbar">
    <div class="container flex">
      <h2 class="logo">Code Factory</h2>
      <ul>
        <li v-for="item in navContent" :key="item.label">
          <!-- <p @click="$router.push(item.route)">{{ item.label }}</p> -->
          <RouterLink :to="item.route">{{ item.label }}</RouterLink>
        </li>
      </ul>
    </div>
  </nav>
</template>

<script>
import { ref } from 'vue'
export default {
  name: 'Footer',

  setup () {
    const navContent = ref ([
      { label: 'Home', route: '/' },
      { label: 'About', route: '/about' },
      { label: 'Projects', route: '/projects' },
      { label: 'Contact', route: '/contact' }
    ])
    return {
      navContent
    }
  }

}
</script>

