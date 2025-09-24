<script setup>
const props = defineProps({
    Title: String,
    Text: String,
    Image: URL,
})
import TextBlock from './TextBlock.vue';
</script>

<template>
    <div class="ImageTextBlock">
        <img :src="Image" />
        <TextBlock :Title="Title" :Text="Text" />
    </div>
</template>

<style scoped>
.ImageTextBlock{
    display: flex;
    flex-direction: row;
    max-width: 70vw;
}
.TextBlock {
    padding: 30px;
}
</style>
