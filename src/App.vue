<script setup>
  import { ref } from "vue";
  import create_action from "./components/create_action.vue"
  import task from "./components/task.vue"

  const tasks = ref([])
</script>

<template>
<h1>nlogn</h1>
<task v-for="t in tasks" :name="t.title" />
<create_action @creation="(task_name)=>{tasks.push({title: task_name})}"/>
</template>