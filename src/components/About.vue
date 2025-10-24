<script setup>
import ImagemSobre from './images/ImagemSobre.vue';
import LinkButtonEatzy from './LinkButtonEatzy.vue';

</script>

<template>
    <section id="about">
        <h1>
            SOBRE O 
            <img src="../assets/EATZY!.svg" alt="EATZY!" class="logo-img-inline">
        </h1> 

        <div class="d-flex">
            <div class="image-wrapper">
                <ImagemSobre />
            </div>
            
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
    display: inline-flex; 
    gap: 15px; 
    align-items: center; 
    font-size: 3rem;
    font-weight: bolder;
    color: black;
    margin: 0 auto 3rem auto; 
}

#about {
    text-align: center;
}

.logo-img-inline {
    width: 150px; 
    vertical-align: middle; 
}

section {
    min-height: 100vh;
    padding: 2rem 5%;
    margin: auto;
    padding-top: 4rem;
}

.d-flex {
    display: flex;
    gap: 40px;
    justify-content: center;
    align-items: center;
}

.image-wrapper {
    flex-shrink: 1; 
    max-width: 50%; 
}

.image-wrapper :deep(img), .image-wrapper :deep(svg) {
    max-width: 100%;
    height: auto;
    display: block;
}


.d-flex > div {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: end; 
    gap: 40px;
    max-width: 500px;
    flex-shrink: 1; 
}

p {
    color: black;
    text-wrap: initial;
}

.texto-1 {
    font-size: 2.5rem;
    width: 100%;
    line-height: 2.8rem;
    text-align: right;
}

.texto-2 {
    font-size: 1.8rem;
    font-weight: bolder;
    text-align: end;
    width: 100%;
    line-height: 2rem;
}

@media (max-width: 1200px) {
    .texto-1 {
        font-size: 2rem;
        line-height: 2.2rem;
    }
    .texto-2 {
        font-size: 1.5rem;
        line-height: 1.7rem;
    }
}

@media (max-width: 992px) {
    h1 {
        font-size: 2.5rem;
        margin-bottom: 2.5rem; 
        gap: 10px;
    }
    .logo-img-inline {
        width: 120px;
    }

    .d-flex {
        flex-direction: column; 
        gap: 30px; 
    }

    .image-wrapper {
        max-width: 100%;
    }

    .d-flex > div {
        align-items: center; 
        text-align: center; 
        max-width: 100%; 
    }

    .texto-1 {
        font-size: 2rem;
        line-height: 2.2rem;
        text-align: center; 
    }
    
    .texto-2 {
        font-size: 1.5rem;
        line-height: 1.7rem;
        text-align: center; 
    }

    section {
        padding: 2rem 20px;
    }
}

@media (max-width: 576px) {
    h1 {
        font-size: 2rem;
        margin-bottom: 2rem;
    }
    .logo-img-inline {
        width: 100px;
    }
    
    section {
        padding-top: 3rem;
    }
    
    .d-flex {
        gap: 20px;
    }
    
    .texto-1 {
        font-size: 1.5rem;
        line-height: 1.7rem;
    }
    .texto-2 {
        font-size: 1.2rem;
        line-height: 1.4rem;
    }
    
    .d-flex > div {
        gap: 20px;
    }
}
</style>