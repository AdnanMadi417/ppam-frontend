<script lang="ts" setup>

const landing = "./images/ppam-logo.png"

</script>

<template>
  <section class="landing-section">
    <div class="content-wrapper">
      <div class="text-container">
        <h2 class="headline">"landing.headline"</h2>
        <p class="subtext">"landing.description"</p>
      </div>
      <div class="image-container">
        <img src="/images/ppam-logo.png" alt="landing-image" class="landing-image" />
      </div>
    </div>
  </section>
</template>

<style scoped>
.landing-section {
  height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  background-image: url("/images/landing-bg.png");
  background-size: cover;
  background-position: center;
  opacity: 0;
  animation: fadeIn 1.5s forwards;
  padding: 1rem;
}

.content-wrapper {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 2rem;
  align-items: center;
  max-width: 1200px;
  width: 100%;
  margin: 0 auto;
}

.image-container {
  display: flex;
  justify-content: center;
  align-items: center;
  opacity: 0;
  animation: slideIn 1.2s ease-out forwards;
}

.landing-image {
  width: 90%;
  max-width: 450px;
  height: auto;
  object-fit: cover;
  border-radius: 10px;
}

.text-container {
  display: flex;
  flex-direction: column;
  justify-content: center;
  opacity: 0;
  animation: fadeIn 1.5s ease-in-out forwards;
  color: var(--text-color);
}

.headline {
  font-size: 2.5rem;
  font-weight: bold;
  margin-bottom: 1rem;
  color: var(--text-color);
}

.subtext {
  font-size: 1rem;
  line-height: 1.6;
  margin-bottom: 1.5rem;
  color: var(--text-color);
}

@media (max-width: 1200px) {
  .content-wrapper {
    grid-template-columns: 1fr;
    text-align: center;
  }

  .landing-image {
    max-width: 80%;
  }

  .headline {
    font-size: 2rem;
  }

  .subtext {
    font-size: 0.95rem;
  }
}

@media (max-width: 768px) {
  .landing-image {
    max-width: 100%;
    height: auto;
  }

  .headline {
    font-size: 1.8rem;
  }

  .subtext {
    font-size: 1rem;
  }
}

@media (max-width: 480px) {
  .headline {
    font-size: 1.5rem;
  }

  .subtext {
    font-size: 0.9rem;
  }
}

@keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}

@keyframes slideIn {
  from {
    transform: translateX(-30px);
    opacity: 0;
  }
  to {
    transform: translateX(0);
    opacity: 1;
  }
}
</style>
