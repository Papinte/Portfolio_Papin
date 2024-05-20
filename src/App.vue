<script setup>
import { RouterLink, RouterView } from 'vue-router'


</script>

<template>
  <header>
    


      <nav>
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/about">About</RouterLink>
      </nav>

  </header>

  <RouterView />
</template>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Titillium+Web:wght@400;700&display=swap');

</style>
