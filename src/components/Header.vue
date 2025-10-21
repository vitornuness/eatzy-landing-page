<script setup>
import LinkButtonEatzy from './LinkButtonEatzy.vue';

</script>

<template>
    <header>
        <div class="header-container">
            <a href="#" class="header-brand">
                <img
                    src="../assets/EATZY!.svg"
                    alt="EATZY!"
                    height="160px"
                >
            </a>

            <nav>
                <ul>
                    <li class="nav-item">
                        <a href="#about" class="nav-link">
                            SOBRE O EATZY
                        </a>
                    </li>
                    <li class="nav-item">
                        <a href="#" class="nav-link">
                            DESCOBRIR <span class="highlight">RESTAURANTES</span>
                        </a>
                    </li>
                    <li class="nav-item">
                        <a href="#" class="nav-link">
                            PARA <span class="highlight">RESTAURANTES</span>
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
    padding-block: 40px;
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
}

nav {
    width: 100%;
}

ul {
    display: flex;
    gap: 80px;
    justify-content: end;
    list-style-type: none;
    width: 100%;
}

a, .nav-link > .highlight {
    font-size: 24px;
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