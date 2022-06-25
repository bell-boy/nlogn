<script setup>
  import { ref } from "vue";
  import create_action from "./components/create_action.vue"
  import task from "./components/task.vue"

  const todo = ref([])
  
  function mes(x)
  {
  	alert(x);
  }
</script>

<template>
<h1>nlogn</h1>
<h2>todo</h2>
<template v-for="t in todo">
	<task v-if="!t.done" :name="t.title" @todo_check="t.done = !t.done" :checked="t.done"/>
</template>
<h2>done</h2>
<template v-for="t in todo">
	<task v-if="t.done" :name="t.title" @todo_check="t.done = !t.done" :checked="t.done"/>
</template>
<create_action @creation="(task_name)=>{todo.push({title: task_name, done: false})}"/>
</template>

