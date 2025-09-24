<script setup>
const props = defineProps({
    Title: String,
    Elements: Array,
})
</script>

<template>
    <div class="BasicList">
        <h1>{{ Title }}</h1>
        <li v-for="element in Elements" :key="element.id">
            {{ element.text }}
        </li>
    </div>

</template>

<style scoped>
.BasicList {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    max-width: 70vw;
}
</style>
