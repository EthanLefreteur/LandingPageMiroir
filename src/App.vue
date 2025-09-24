<script setup>
import HeaderMenu from './components/HeaderMenu.vue';
import TextBlock from './components/TextBlock.vue';
import ImageTextBlock from './components/ImageTextBlock.vue';
import Space from './components/Space.vue';
import BasicList from './components/BasicList.vue';
import image from "./assets/mirror.jpg"

const buttons = [
  { text: "Top Page", id: "button_1", callback: () => { scrollToAnchor("top") } },
  { text: "Bottom Page", id: "button_2", callback: () => { scrollToAnchor("contact") } }
]

const SpecsList = [
  {text: "Raspberry Pi 4", id: "spec_1"},
  {text: "ESP32", id: "spec_2"},
  {text: "Capteur de température SHTC3", id: "spec_3"},
  {text: "Detecteur de présence", id: "spec_4"},
  {text: "Écran 1920x1080", id: "spec_5"},
  
]

function scrollToAnchor(id) {
  const target = document.getElementById(id);
  const targetPosition = target.getBoundingClientRect().top + window.pageYOffset;
  window.scrollTo({
    top: targetPosition,
    behavior: 'smooth'
  });
}

</script>

<template>
  <header>
    <HeaderMenu :Buttons="buttons" Title="Smart Mirror" id="header" />
  </header>

  <main>
    <Space space="200px" id="top"/>
    <TextBlock Title="Le Miroir du futur"
      Text="Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum." />
    <Space space="100px" />

    <ImageTextBlock Title="Bien plus qu'un miroir"
      Text="Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum."
      :Image="image"
    />
      
    <Space space="100px" />
    <BasicList Title="Composants du miroir"
      :Elements=SpecsList />
    <Space space="100px" />
    <TextBlock Title="Contactez nous !"
      Text="Lorem ipsum dolor sit amet !" id="contact"/>
    <Space space="100px" />
  </main>
</template>

<style>
body {
  justify-content: center;
  align-items: start;
  min-height: auto;
  background: rgb(30, 30, 30);
  margin: 0;
  box-sizing: unset;
}

#app {
  display: flex;
  flex-direction: column;
  justify-content: start;
  align-items: center;
  min-height: auto;
  width: 100vw;
  max-width: 100%;
  padding: 0;
  margin: 0;
}
</style>

<style scoped>
header {
  top: 0;
  position: fixed;
  height: 100px;
  width: 100%;
  background: black;
  align-items: center;
  justify-content: center;
  display: flex;
  flex-direction: row;
}
</style>
