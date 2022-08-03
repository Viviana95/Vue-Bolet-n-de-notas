<script setup>
import { RouterLink, RouterView } from 'vue-router'

</script>

<template>
<nav class="navbar navbar-dark bg-dark navbar-expand-lg ">
 <RouterLink to="/">Home</RouterLink>
 <RouterLink to="/report">Report</RouterLink>
</nav>


  
 

  <RouterView />
</template>

<style scoped>

</style>
