<script setup>
    import { ref, watch } from 'vue'
    const props = defineProps(['name','checked'])
	const emit = defineEmits([])
</script>

<template>
    <span>{{ name }}</span>
	<input type="checkbox" @change="$emit('todo_check')" :checked="props.checked">
	<br>
</template>
