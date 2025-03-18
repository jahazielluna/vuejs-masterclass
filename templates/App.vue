<script setup lang="ts">
import SideBar from './components/ui/Layout/SideBar.vue'
import TopNavbar from './components/ui/Layout/TopNavbar.vue'
</script>

<template>
  <SideBar />
  <div class="flex flex-col lg:ml-52 ml-16 transition-[margin]">
    <TopNavbar />
    <main>
      <RouterView />
    </main>
  </div>
</template>
