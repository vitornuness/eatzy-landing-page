<script setup>
</script>

<template>
  <section id="para-restaurantes">
    <div class="content">
      <div class="text-section">
        <h2 class="title-primary">
          PARA <span class="text-red">RESTAURANTES</span>
        </h2>

        <p class="benefits">
          + <span class="text-red">VISIBILIDADE</span> + <span class="text-red">CLIENTES</span>
        </p>

        <h3 class="call-to-action">
          Faça seu estabelecimento aparecer no mapa.
        </h3>

        <p class="description">
          Com o Eatzy, seu restaurante aparece para quem está com fome aí perto.
        </p>

        <p class="signup-prompt">
          Cadastre-se ou entre em contato conosco.
        </p>
      </div>

      <div class="contact-section">
        <div class="contact-button phone-button">
          <svg xmlns="http://www.w3.org/2000/svg" width="25" height="25" fill="currentColor" class="bi bi-telephone-fill" viewBox="0 0 16 16">
            <path fill-rule="evenodd" d="M1.885.511a1.745 1.745 0 0 1 2.61.163L6.29 2.98c.329.423.445.974.315 1.494l-.547 2.19a.68.68 0 0 0 .178.643l2.457 2.457a.68.68 0 0 0 .644.178l2.189-.547a1.75 1.75 0 0 1 1.494.315l2.306 1.794c.829.645.905 1.87.163 2.611l-1.034 1.034c-.74.74-1.846 1.065-2.877.702a18.6 18.6 0 0 1-7.01-4.42 18.6 18.6 0 0 1-4.42-7.009c-.362-1.03-.037-2.137.703-2.877z"/>
          </svg>
          <span>14 99999-9999</span>
        </div>

        <div class="contact-button email-button">
          <svg xmlns="http://www.w3.org/2000/svg" width="25" height="25" fill="currentColor" class="bi bi-envelope" viewBox="0 0 16 16">
            <path d="M0 4a2 2 0 0 1 2-2h12a2 2 0 0 1 2 2v8a2 2 0 0 1-2 2H2a2 2 0 0 1-2-2zm2-1a1 1 0 0 0-1 1v.217l7 4.2 7-4.2V4a1 1 0 0 0-1-1zm13 2.383-4.708 2.825L15 11.105zm-.034 6.876-5.64-3.471L8 9.583l-1.326-.795-5.64 3.47A1 1 0 0 0 2 13h12a1 1 0 0 0 .966-.741M1 11.105l4.708-2.897L1 5.383z"/>
          </svg>
          <span>
            eatzy@gmail.br
          </span> 
        </div>

        <a href="https://eatzyy.vercel.app/" class="eatzy-link">IR PARA O EATZY</a>
      </div>
    </div>
  </section>
</template>

<style scoped>
:root {
  --color-yellow: #f8e58a;
  --color-red: #c62e2e;
  --color-text: #000;
  --font-family-bold: 'Arial Black', sans-serif;
}

#para-restaurantes {
  width: 100%;
  background-color: var(--color-yellow);
  display: flex;
  justify-content: center;
  align-items: flex-start;
  padding: 80px 40px;
  box-sizing: border-box;
  font-family: Arial, sans-serif;
  font-weight: 400;
  position: relative;
}

.content {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  max-width: 1100px;
  width: 100%;
  gap: 30px;
}

.text-section {
  flex-basis: 60%;
  min-width: 300px;
  color: var(--color-text);
}

.title-primary {
  font-size: 3.5rem;
  font-weight: 900;
  font-family: var(--font-family-bold);
  margin: 0 0 5px 0;
  line-height: 1;
}

.text-red {
  color: var(--color-red);
}

.benefits {
  font-size: 2rem;
  font-weight: 900;
  font-family: var(--font-family-bold);
  margin: 0 0 40px 0;
  line-height: 1;
}

.call-to-action {
  font-size: 2.5rem;
  font-weight: 900;
  margin: 0 0 20px 0;
  line-height: 1.2;
  max-width: 90%;
}

.description {
  font-size: 1.4rem;
  font-weight: 400;
  margin: 0 0 80px 0;
  line-height: 1.4;
  max-width: 80%;
}

.signup-prompt {
  font-weight: 700;
  font-size: 1.2rem;
  position: absolute;
  bottom: 40px; 
  left: 40px;
}

.contact-section {
  flex-basis: 40%;
  min-width: 300px;
  display: flex;
  flex-direction: column;
  align-items: flex-end; 
  gap: 20px;
}

.contact-button {
  color: #fff;
  font-weight: 700;
  font-size: 1.5rem;
  padding: 15px 30px;
  border-radius: 8px;
  width: 300px; 
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 10px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.2);
}

.phone-button {
  background-color: var(--color-red);
  color: #000;
}

.email-button {
  background-color: #a82727; 
  font-size: 1.3rem;
  padding: 20px 30px;
}

.eatzy-link {
  text-decoration: none;
  color: var(--color-red);
  font-size: 1.1rem;
  font-weight: 900;
  margin-top: 10px;
  align-self: flex-end; 
}

@media (max-width: 992px) {
  #para-restaurantes {
    padding: 60px 30px 120px;
  }
  
  .content {
    flex-direction: column;
    align-items: center;
  }

  .text-section {
    max-width: 100%;
    text-align: center;
  }

  .title-primary, .benefits, .call-to-action, .description {
    max-width: 100%;
    margin-left: auto;
    margin-right: auto;
  }

  .contact-section {
    align-items: center;
    width: 100%;
    margin-top: 20px;
  }

  .contact-button {
    width: 80%;
    max-width: 340px;
  }

  .eatzy-link {
    align-self: center;
  }
  
  .signup-prompt {
    position: absolute;
    bottom: 40px;
    left: 50%;
    transform: translateX(-50%);
    text-align: center;
    width: 90%;
  }
}

@media (max-width: 600px) {
  #para-restaurantes {
    padding: 40px 20px 100px;
  }
  
  .title-primary {
    font-size: 2.5rem;
  }

  .benefits {
    font-size: 1.5rem;
    margin-bottom: 30px;
  }

  .call-to-action {
    font-size: 1.8rem;
  }

  .description {
    font-size: 1.1rem;
    margin-bottom: 50px;
  }

  .contact-button {
    font-size: 1.2rem;
    padding: 12px 20px;
    width: 100%;
    max-width: 280px;
  }
  
  .email-button {
    font-size: 1.1rem;
    padding: 15px 20px;
  }

  .signup-prompt {
    font-size: 1rem;
    bottom: 20px;
  }
}
</style>