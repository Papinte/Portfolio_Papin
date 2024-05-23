<template>
<div>
  <RouterLink to="/">HomePage</RouterLink>
  <RouterLink to="/about">About</RouterLink>
</div>
<RouterView />

</template>

<script setup>
import { RouterLink, RouterView } from 'vue-router'




</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Titillium+Web:wght@400;700&display=swap');

</style>
