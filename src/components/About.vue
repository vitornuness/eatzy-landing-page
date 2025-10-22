<script setup>
import ImagemSobre from './images/ImagemSobre.vue';
import LinkButtonEatzy from './LinkButtonEatzy.vue';

</script>

<template>
    <section id="about">
        <h1>SOBRE O <img src="../assets/EATZY!.svg" alt="EATZY!" width="180px"></h1>

        <div class="d-flex">
            <ImagemSobre />
            <div>
                <p class="texto-1">
                    Nossa plataforma <br>
                    facilita a conexão de <br>
                    estabelecimentos e clientes.
                </p>

                <p class="texto-2">
                    Acesse agora e descubra os <br>
                    restaurantes próximos à você!
                </p>

                <div class="big-button">
                    <LinkButtonEatzy bigButton="true" />
                </div>
            </div>
        </div>
    </section>
</template>

<style scoped>
h1 {
    position: relative;
    font-size: 40pt;
    font-weight: bolder;
    color: black;
    margin-bottom: 20px;
}

h1 > img {
    position: absolute;
    bottom: -45px;
}

section {
    min-height: 100vh;
    padding-inline: 80px;
    padding-block: 20px;
    margin: auto;
    padding-top: 40px;
/* 
    border-top: 48px dashed #e60012;
    border-left: 48px dashed #e60012;
    border-top-right-radius: 0;
    border-bottom-left-radius: 0;
    border-bottom-right-radius: 0;
    border-spacing: 10px; */
}

.d-flex {
    display: flex;
    gap: 40px;
}

.d-flex > div {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: end;
    gap: 40px;
}

p {
    color: black;
    text-wrap: nowrap;
}

.texto-1 {
    font-size: 40pt;
    width: 100%;
    line-height: 40pt;
}

.texto-2 {
    font-size: 28pt;
    font-weight: bolder;
    text-align: end;
    width: 100%;
    line-height: 28pt;
}
</style>