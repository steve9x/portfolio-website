<template>
  <div class="home-wrapper">
    <div class="container">
      <div class="home-content">
        <p class="fs-600 fw-regular">Welcome to the</p>
        <h1 class="fs-primary-heading fw-bold ">Code Factory</h1>
        <h2 class="fs-secondary-heading fw-semi-bold">Full Stack Developer</h2>
      </div>
      <div class="home-btn flex">
        <button @click="$router.push('/projects')" class="button" >Go to Projects</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Home'
}
</script>
