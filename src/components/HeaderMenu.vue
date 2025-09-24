<script setup>
    const props = defineProps({
        Buttons: Array,
    })
</script>

<template>
    <a v-for="button in Buttons" :key="button.id" @click="button.callback">{{ button.text }}</a>
</template>

<style scoped>
a {
    color: white;
    background: rgb(30, 30, 30);
    margin-left: 10px;
    margin-right: 10px;
    
}
</style>
