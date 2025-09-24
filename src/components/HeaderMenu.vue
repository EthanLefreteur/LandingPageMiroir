<script setup>
    const props = defineProps({
        Title: String,
        Buttons: Array,
    })
</script>

<template>
    <p>{{ Title }}</p>
    <a v-for="button in Buttons" :key="button.id" @click="button.callback">{{ button.text }}</a>
</template>

<style scoped>
a {
    color: white;
    background: rgb(30, 30, 30);
    margin-left: 10px;
    margin-right: 10px;
    cursor: pointer;
    border-radius: 8px;
    border-style: none;
    padding: 5px;
    font-size: 20px;
}

p {
    font-size: 50px;
    position: absolute;
    left: 0;
    margin-left: 25px;
    color: white;
}

</style>
