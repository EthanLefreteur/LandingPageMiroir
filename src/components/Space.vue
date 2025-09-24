<script setup>
    const props = defineProps({
        space: Number
    })
</script>

<template>
    <p></p>
</template>

<style scoped>
p {
    height: v-bind(space);
}
</style>
