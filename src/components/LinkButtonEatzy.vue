<script setup>
defineProps({
    bigButton: false
});
</script>

<template>
    <a href="https://eatzyy.vercel.app" :class="bigButton ? 'big-button' : ''">
        IR PARA O EATZY
    </a>
</template>

<style scoped>
a {
    font-size: 24px;
    font-weight: bold;
    background: none;
    background-color: red;
    color: white;
    border-radius: 12px;
    padding: 12px;
}

.big-button, .big-button:hover {
    font-size: 36pt;
    padding: 20px 40px;
}

a:hover {
    background: none;
    background-color: red !important;
    color: white;
    border-radius: 12px;
    padding: 12px;
}
</style>