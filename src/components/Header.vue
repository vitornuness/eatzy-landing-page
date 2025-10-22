<script setup>
import LinkButtonEatzy from './LinkButtonEatzy.vue';

</script>

<template>
    <header>
        <div class="header-container">
            <a href="#" class="header-brand">
                <img
                    src="../assets/logo-eatzy.png"
                    alt="EATZY!"
                    height="60px"
                >
            </a>

            <nav>
                <ul>
                    <li class="nav-item">
                        <a href="#about" class="nav-link">
                            <span class="highlight">SOBRE O EATZY</span>
                        </a>
                    </li>
                    <li class="nav-item">
                        <a href="#descobrirRestaurantes" class="nav-link">
                            <span class="highlight">DESCOBRIR RESTAURANTES</span>
                        </a>
                    </li>
                    <li class="nav-item">
                        <a href="#" class="nav-link">
                            <span class="highlight">PARA RESTAURANTES</span>
                        </a>
                    </li>
                    <li>
                        <LinkButtonEatzy />
                    </li>
                </ul>
            </nav>
        </div>
    </header>
</template>

<style scoped>
header {
    position: absolute;
    top: 0;
    right: 0;
    width: 100%;
    z-index: 9999;
}

.header-container {
    margin: 12px;
    padding-block: 25px;
    padding-inline: 24px;
    background-color: #ffffff80;
    border-radius: 20px;
    box-shadow: #00000033 2px 2px 10px;

    display: flex;
    align-items: center;
    justify-content: space-between;
}

.header-brand {
    position: absolute;
    display: flex;
    justify-content: center;
    align-items: center;
}

nav {
    width: 100%;
}

ul {
    display: flex;
    gap: 20px;
    justify-content: end;
    list-style-type: none;
    width: 100%;
}

a, .nav-link > .highlight {
    font-size: 18px;
    font-weight: bold;
}

a:hover {
    background: none;
}

.nav-link {
    color: black;
}

.nav-link:active {
    color: red;
}

.nav-link:hover > .highlight {
    color: red;
}
</style>