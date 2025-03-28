<script setup lang="ts">
  usePageStore().pageData.title = 'Homepage';
</script>

<template>
    <div>
      <h1>Home Page</h1>
      <RouterLink to="/projects">Projects</RouterLink><br>
      <RouterLink to="/tasks">Tasks</RouterLink>
    </div>
</template>

<style scoped>
</style>
