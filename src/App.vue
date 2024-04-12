<script setup>

import {onMounted, ref} from "vue";
import WebApp from "@twa-dev/sdk";

const counter = ref(0);

onMounted(() => {
  WebApp.expand();
})

function incrementCounter() {
  counter.value += 1
}

</script>

<template>
  <div class="app-container">
    <div class="counter roboto-bold" >{{ counter }}</div>
    <img @click="incrementCounter" alt="Vue logo" class="ment" src="@/assets/img/sticker.webp" width="512" height="512"/>
    <div class="counter">{{ username }}</div>
  </div>
</template>

<style scoped>
.app-container {
  background: #222222;
  height: 100dvh;
  width: 100dvw;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  user-select: none;
}

.counter {
  font-size: 3rem;
  color: white;
  font-family: "Roboto", sans-serif;
  font-weight: 700;
  padding: 3rem 1rem;
}

.ment {

}

.ment:hover, .ment:active {
  scale: 0.9;
}


@media (min-width: 1024px) {

}
</style>
