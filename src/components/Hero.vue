<script setup>
import { ref, onMounted, onUnmounted } from 'vue'

import hero1 from '../assets/Hero.png'
import hero2 from '../assets/hero2.png'

const images = [hero1, hero2]

const currentIndex = ref(0)
let intervalId = null

/* Troca automática
onMounted(() => {
  intervalId = setInterval(() => {
    currentIndex.value = (currentIndex.value + 1) % images.length
  }, 7000)
})*/

onUnmounted(() => {
  clearInterval(intervalId)
})

// Controle manual
function nextSlide() {
  currentIndex.value = (currentIndex.value + 1) % images.length
}

function prevSlide() {
  currentIndex.value =
    (currentIndex.value - 1 + images.length) % images.length
}
</script>

<template>
  <div class="container full-screen">
    <transition name="fade" mode="out-in">
      <img
        :key="images[currentIndex]"
        :src="images[currentIndex]"
        alt="Imagem do carrossel Eatzy"
      >
    </transition>

    <button class="prev" @click="prevSlide">
        <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" fill="currentColor" class="bi bi-chevron-left" viewBox="0 0 16 16">
            <path fill-rule="evenodd" d="M11.354 1.646a.5.5 0 0 1 0 .708L5.707 8l5.647 5.646a.5.5 0 0 1-.708.708l-6-6a.5.5 0 0 1 0-.708l6-6a.5.5 0 0 1 .708 0"/>
        </svg>
    </button>
    <button class="next" @click="nextSlide">
        <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" fill="currentColor" class="bi bi-chevron-right" viewBox="0 0 16 16">
            <path fill-rule="evenodd" d="M4.646 1.646a.5.5 0 0 1 .708 0l6 6a.5.5 0 0 1 0 .708l-6 6a.5.5 0 0 1-.708-.708L10.293 8 4.646 2.354a.5.5 0 0 1 0-.708"/>
        </svg>
    </button>
  </div>
</template>

<style scoped>
.container {
  position: relative;
  overflow: hidden;
  z-index: 1;
  margin: 12px;
  border-radius: 20px;
}

.full-screen {
  /*width: 100vw;
  height: 100vh;*/
  z-index: 1;
}

.full-screen img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  display: block;
}

button {
  position: absolute;
  top: 50%;
  height: 40px;
  width: 40px;
  transform: translateY(-50%);
  background-color: rgba(255, 255, 255, 0.5);
  border: none;
  font-size: 2.5rem;
  cursor: pointer;
  border-radius: 50%;
  transition: background 0.3s;
  user-select: none;
  display: flex;
  justify-content: center;
  align-items: center;
}

button:hover {
  background-color: rgba(255, 255, 255, 0.9);
}

.prev {
  left: 20px;
}

.next {
  right: 20px;
}

</style>
