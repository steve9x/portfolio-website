<template>
  <div class="projects-wrapper flex">
    <div class="container flex">
      <div class="cards-wrapper flex">
        <div v-for="project in projects" :key="project.name" class="card">
          <div class="img-container">
            <img :src="require(`@/assets/${project.img}`)" alt="" />
          </div>
          <h2 class="fs-secondary-heading">{{ project.name }}</h2>
          <hr class="thin">
          <p>{{ project.desciption }}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { ref } from 'vue'
export default {
  name: 'Projects',
  setup () {
    const projects = ref ([
      {name: 'Intel Realsense', desciption: 'A Computer Vison programm to detect and locate Objects \
        in a filmed room. Using tools like C++ and OpenCV', img: 'realsense.jpg'},
      {name: 'Wooden Robot', desciption: 'A Tea robot which makes you a tea. Using tools like C++ \
        and ArduinoUno', img: 'woodrobot.webp'},
      {name: 'Portfolio Website', desciption: 'Portfolio Website for me as Web Developer. Using tools \
      like Vuejs framework and vanilla css', img: 'background.jpg'}
    ])
    return {
      projects
    }
  }
}
</script>
