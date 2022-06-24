<script setup>
  import { ref } from "vue";
  import create_action from "./components/create_action.vue"
  import task from "./components/task.vue"

  const todo = ref([])
</script>

<template>
<h1>nlogn</h1>
<h2>todo</h2>
<template v-for="t in todo">
	<task :name="t.title" />
</template>
<h2>done</h2>
<create_action @creation="(task_name)=>{todo.push({title: task_name})}"/>
</template>

<!-- TODO: create switching from todo task done -->
