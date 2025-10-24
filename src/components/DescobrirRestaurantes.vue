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
        
<div class="row">
            <div class="col left-content">
                <h1>DESCOBRIR <span class="highlight">RESTAURANTES</span></h1>
                <p>Nunca foi tão fácil!</p>
                <div>
                    <LinkButtonEatzy buttonText="IR PARA O EATZY" />
                </div>
            </div>
            <div class="col carousel-column">
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
    padding: 3rem 5%;
    width: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: flex-start;
}

.row {
    display: flex;
    width: 100%;
    gap: 50px;
    align-items: center;
    justify-content: center;
}

.col {
    display: flex;
    flex-direction: column;
    justify-content: center;
    width: 100%;
}

.left-content {
    flex: 0 0 45%;
    max-width: 45%;
    align-items: flex-start;
    gap: 1.5rem;
}

h1 {
    font-weight: 800;
    color: #333;
    font-size: 3rem;
    text-align: left;
    margin-bottom: 0.5rem;
    line-height: 1.1;
    text-transform: uppercase;
}

p {
    font-size: 2.2rem;
    color: #333;
    font-weight: 600;
    text-wrap: initial;
    line-height: 1.1;
    margin-bottom: 2rem;
}

.highlight {
    color: #FF4500;
    font-weight: 800;
}

:deep(.link-button-eatzy) {
    background-color: #FF4500;
    color: white;
    padding: 1rem 2rem;
    border-radius: 5px;
    font-weight: 700;
    font-size: 1.1rem;
    text-decoration: none;
    transition: background-color 0.3s ease;
}

:deep(.link-button-eatzy:hover) {
    background-color: #e63900;
}

.carousel-column {
    flex: 0 0 55%;
    max-width: 55%;
    display: flex;
    justify-content: center;
}

.carousel-container {
    position: relative;
    width: 100%;
    max-width: 550px;
    margin: 0;
    overflow: hidden;
    border-radius: 10px;
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
    background-color: #f8f8f8;
    border: 1px solid #eee;
}

.carousel {
    display: flex;
    /* CORREÇÃO: Remove overflow-x: hidden para permitir que o scroll() funcione via JS */
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
    padding: 30px;
    min-height: 300px;
}

.slide > :deep(*) { 
    max-width: 100%;
    height: auto;
    display: block;
}

.carousel-btn {
    /* Tornando os botões funcionais e discretos */
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
    background: rgba(255, 255, 255, 0.5);
    border: none;
    font-size: 1.5rem;
    color: #FF4500;
    cursor: pointer;
    padding: 0.5rem 0.8rem;
    border-radius: 50%;
    z-index: 10;
    transition: all 0.2s ease-in-out;
    width: 45px;
    height: 45px;
    display: flex;
    justify-content: center;
    align-items: center;
    font-weight: 700;
}

.carousel-btn:hover {
    background: rgba(255, 255, 255, 0.9);
    color: #FF4500;
}

.carousel-btn.prev {
    left: 10px;
}

.carousel-btn.next {
    right: 10px;
}

@media (max-width: 1200px) {
    .left-content {
        flex: 0 0 40%;
        max-width: 40%;
    }
    .carousel-column {
        flex: 0 0 60%;
        max-width: 60%;
    }
}

@media (max-width: 992px) {
    section {
        padding: 3rem 5%;
    }
    .row {
        flex-direction: column;
        gap: 2rem;
    }

    .left-content,
    .carousel-column {
        flex: 0 0 100%;
        max-width: 100%;
        align-items: center;
        text-align: center;
    }

    h1 {
        font-size: 2.5rem;
        text-align: center;
    }

    p {
        font-size: 1.8rem;
        text-align: center;
    }

    .carousel-container {
        width: 90%;
        max-width: 450px;
        margin-top: 1rem;
    }
    .slide {
        padding: 20px;
        min-height: 250px;
    }
    .carousel-btn {
        width: 35px;
        height: 35px;
        font-size: 0.9rem;
    }
}

@media (max-width: 576px) {
    section {
        padding: 2rem 5%;
    }

    h1 {
        font-size: 2rem;
    }

    p {
        font-size: 1.5rem;
    }
    
    .carousel-container {
        width: 100%;
        max-width: 350px;
    }
    .slide {
        padding: 15px;
        min-height: 200px;
    }
    .carousel-btn {
        width: 30px;
        height: 30px;
        font-size: 0.8rem;
    }
}
</style>