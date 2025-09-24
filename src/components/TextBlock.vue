<script setup>
    const props = defineProps({
        Title: String,
        Text: String,
    })
</script>

<template>
    <div class="TextBlock">
        <h1>{{ Title }}</h1>
        <p>{{ Text }}</p>
    </div>
    
</template>

<style scoped>
    .TextBlock {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        max-width: 70vw;
    }
</style>
