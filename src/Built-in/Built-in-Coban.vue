<template>
    <h1>Built-in Components</h1>
</template>

<script setup>
    import { ref } from 'vue'
    
    const message = ref('Test console.log')
    console.log(message.value)
</script>