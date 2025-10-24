<script setup>
import { ref } from 'vue';
import LinkButtonEatzy from './LinkButtonEatzy.vue';

const isMenuOpen = ref(false);

function toggleMenu() {
    isMenuOpen.value = !isMenuOpen.value;
}
</script>

<template>
    <header>
        <div class="header-container">
            <a href="#" class="header-brand">
                <img
                    src="../assets/logo-eatzy.png"
                    alt="EATZY!"
                    height="40"
                >
            </a>

            <button class="menu-toggle" @click="toggleMenu">
                <span class="bar"></span>
                <span class="bar"></span>
                <span class="bar"></span>
            </button>

            <nav :class="{ 'open': isMenuOpen }">
                <ul>
                    <li class="nav-item" @click="isMenuOpen = false">
                        <a href="#about" class="nav-link">
                            <span class="highlight">SOBRE O EATZY</span>
                        </a>
                    </li>
                    <li class="nav-item" @click="isMenuOpen = false">
                        <a href="#descobrirRestaurantes" class="nav-link">
                            <span class="highlight">DESCOBRIR RESTAURANTES</span>
                        </a>
                    </li>
                    <li class="nav-item" @click="isMenuOpen = false">
                        <a href="#" class="nav-link">
                            <span class="highlight">PARA RESTAURANTES</span>
                        </a>
                    </li>
                    <li @click="isMenuOpen = false">
                        <LinkButtonEatzy />
                    </li>
                </ul>
            </nav>
        </div>
    </header>
</template>

<style scoped>
header {
    position: fixed;
    top: 0;
    right: 0;
    width: 100%;
    z-index: 9999;
}

.header-container {
    margin: 1rem;
    padding: 1rem 1.5rem;
    background-color: #ffffff80;
    border-radius: 1.25rem;
    box-shadow: #00000033 2px 2px 10px;    
    display: flex;
    align-items: center;
    justify-content: space-between;
}

.header-brand img {
    height: 3rem;
    width: auto;
}

.menu-toggle {
    display: none;
    background: none;
    border: none;
    cursor: pointer;
    padding: 0.5rem;
    z-index: 10000;
}

.bar {
    display: block;
    width: 25px;
    height: 3px;
    margin: 5px auto;
    background-color: black;
    transition: all 0.3s ease-in-out;
}

nav {
    width: auto;
}

ul {
    display: flex;
    gap: 1.25rem;
    justify-content: end;
    list-style-type: none;
    padding: 0;
    margin: 0;
}

a, .nav-link > .highlight {
    font-size: 1rem;
    font-weight: bold;
    white-space: nowrap;
    text-decoration: none;
}

a:hover {
    background: none;
}

.nav-link {
    color: black;
    padding: 0.5rem;
}

.nav-link:active {
    color: red;
}

.nav-link:hover > .highlight {
    color: red;
}

@media (max-width: 992px) {
    .menu-toggle {
        display: block;
    }

    nav {
        display: none;
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100vh;
        background-color: rgba(255, 255, 255, 0.95);
        padding-top: 5rem;
        transition: transform 0.3s ease-in-out;
        transform: translateX(-100%);
    }

    nav.open {
        display: flex;
        align-items: flex-start;
        justify-content: center;
        transform: translateX(0);
    }

    ul {
        flex-direction: column;
        align-items: center;
        gap: 1.5rem;
        padding-top: 3rem;
        width: 100%;
    }

    .nav-item {
        margin: 0.5rem 0;
    }

    a, .nav-link > .highlight {
        font-size: 1.5rem;
        color: black;
    }

    .header-container {
        margin: 0.5rem;
        padding: 0.75rem 1rem;
    }
}
</style>