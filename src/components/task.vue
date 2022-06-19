<script setup>
    import { ref } from 'vue'
    const props = defineProps(['name'])
</script>

<template>
    <p>{{ name }}</p>
</template>