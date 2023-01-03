<template >
  <div class="primary-header">
    <div class="container flex">
      <div class="nav-wrapper">
        <h2 class="fs-secondary-heading">Code Factory</h2>
        <nav class="primary-navigation">
          <ul class="nav-list" role="list">
            <li v-for="item in navContent" :key="item.label" class="nav-item">
              <RouterLink :to="item.route" tag="a">{{ item.label }}</RouterLink>
            </li>
          </ul>
        </nav>
      </div>
    </div>
  <hr class="thin container">
  </div>
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

