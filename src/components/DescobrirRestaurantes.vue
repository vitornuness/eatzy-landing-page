<script setup>
import { ref } from 'vue';
import ConfigureSuaLocalizacao from './images/ConfigureSuaLocalizacao.vue';
import MostrarMelhorRota from './images/MostrarMelhorRota.vue';
import SelecioneEstabelecimento from './images/SelecioneEstabelecimento.vue';
import SelecioneSuaComida from './images/SelecioneSuaComida.vue';
import LinkButtonEatzy from './LinkButtonEatzy.vue';

const carousel = ref(null)

function scroll(direction) {
  const el = carousel.value
  if (!el) return
  const width = el.clientWidth
  el.scrollBy({
    left: direction * width,
    behavior: 'smooth'
  })
}
</script>

<template>
    <section id="descobrirRestaurantes">
        <h1>DESCOBRIR <span class="highlight">RESTAURANTES</span></h1>

        <div class="row">
            <div class="col fit">
                <p>
                    Nunca foi tão fácil!
                </p>
                <div>
                    <LinkButtonEatzy bigButton="true" />
                </div>
            </div>
            <div class="col">
                <div class="carousel-container">
                    <button class="carousel-btn prev" @click="scroll(-1)">❮</button>

                    <div ref="carousel" class="carousel">
                        <div class="slide"><ConfigureSuaLocalizacao /></div>
                        <div class="slide"><SelecioneSuaComida /></div>
                        <div class="slide"><SelecioneEstabelecimento /></div>
                        <div class="slide"><MostrarMelhorRota /></div>
                    </div>

                    <button class="carousel-btn next" @click="scroll(1)">❯</button>
                </div>
            </div>
        </div>
    </section>
</template>

<style scoped>
section {
    min-height: 100vh;
    padding: 40px 80px;
    width: 100%;

    display: flex;
    flex-direction: column;
    justify-content: center;
}

h1 {
    font-weight: bolder;
    color: black;
    font-size: 32pt;
}

p {
    font-size: 48pt;
    color: black;
    text-wrap: nowrap;
}

section > div {
    padding-block: 40px;
}

.highlight {
    color: red;
    font-weight: bold;
}

.row {
    display: flex;
    width: 100%;
    gap: 40px;
}

.col {
    display: flex;
    flex-direction: column;
    justify-content: center;
    gap: 40px;
    width: 100%;
}

.fit {
    width: fit-content;
}

.carousel-container {
  position: relative;
  width: 100%;
  overflow: hidden;
}

.carousel {
  display: flex;
  overflow-x: auto;
  scroll-snap-type: x mandatory;
  scroll-behavior: smooth;
  scrollbar-width: none;
  -ms-overflow-style: none;
}

.carousel::-webkit-scrollbar {
  display: none;
}

.slide {
  flex: 0 0 100%;
  scroll-snap-align: start;
  display: flex;
  justify-content: center;
  align-items: center;
}

.carousel-btn {
  position: absolute;
  bottom: 10%;
  transform: translateY(-50%);
  background: none;
  border: none;
  font-size: 2rem;
  cursor: pointer;
  padding: 0.5rem 1rem;
  border-radius: 50%;
}

.carousel-btn.prev {
  left: 0;
}

.carousel-btn.next {
  right: 0;
}

</style>