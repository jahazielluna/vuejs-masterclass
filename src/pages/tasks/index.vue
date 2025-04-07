<script setup lang="ts">
import { taskWithProjectsQuery, type TaskWithProjects } from '@/utils/supaQueries';
import { columns } from '@/utils/tableColumns/taskColumns';

usePageStore().pageData.title = 'MyTasks';


let tasks = ref<TaskWithProjects | null>(null)
const getTasks =async ()=> {
  const { data, error, status } = await taskWithProjectsQuery
    
    if (error) useErrorStore().setError({ error, customCode: status})
    tasks.value = data
}
await getTasks();
</script>

<template>
  <DataTable v-if="tasks" :columns="columns" :data="tasks" />
</template>

<style scoped>
</style>