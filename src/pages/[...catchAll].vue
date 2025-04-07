<script setup lang="ts">
import { useErrorStore } from '@/store/error';

useErrorStore().setError({ error: 'Page not found', customCode: 404 });
</script>

<template>
  <div>
  </div>
</template>
  
  <style scoped>
  
  </style>