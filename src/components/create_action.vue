<script setup>
    import {ref} from 'vue'
    const emit = defineEmits(["creation"])


    const task_name_input = ref(null)
    function creation() {
        if(task_name_input.value != null)
        {
            emit("creation",task_name_input.value.value)
            task_name_input.value.value=""
        }
    }
</script>

<template>
    <label for="task_name">Task Name </label>
    <input type="text" id="task_name" placeholder="type task name here" ref="task_name_input">
    <br />
    <button @click="creation">create task</button>
</template>