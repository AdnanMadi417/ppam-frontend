<script setup lang="ts">
const information = [
  {
    title: "Vision",
    description:
        "To be a leading support hub for Palestinian students in Malaysia, fostering academic excellence, personal growth, and cultural pride, while strengthening the bonds of solidarity within the Palestinian community."
  },
  {
    title: "Mission",
    description:
        "To provide educational, social, and emotional support to Palestinian students studying in Malaysia.\n" +
        "To create a strong network that connects Palestinian students with academic, professional, and community opportunities.\n" +
        "To preserve and promote Palestinian identity, heritage, and values among the student community."
  }
];

const images = [
  {
    url: "./images/landing-bg.png",
    alt: "WB-5core-values"
  }
];
</script>

<template>
  <section class="ppam-about-section">
    <div class="ppam-about-container">
      <h1 class="ppam-about-title">About Palestinian Progressive Association Malaysia</h1>
      <hr class="ppam-divider"/>

      <div class="ppam-information">
        <div v-for="info in information" :key="info.title" class="ppam-info-card">
          <h3 class="ppam-info-title">{{ info.title }}</h3>
          <p class="ppam-info-description">{{ info.description }}</p>
        </div>
      </div>

      <div class="ppam-images">
        <div v-for="image in images" :key="image.url" class="ppam-image-wrapper">
          <img :src="image.url" :alt="image.alt" class="ppam-image"/>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
section {
  padding: 5em;
  margin: 1em auto;
}

.ppam-about-container {
  max-width: 1200px;
}

.ppam-about-title {
  font-size: 2.5rem;
  margin-left: 20px;
  color: var(--primary-hover);
}

@media (max-width: 800px) {
  .ppam-about-section {
    padding: 2rem 1rem;
  }

  .ppam-about-title {
    font-size: 1.2rem;
  }
}

.ppam-divider {
  margin: 1rem auto;
  border: 2px solid var(--primary-color);
  width: 100%;
}

.ppam-information {
  display: flex;
  justify-content: space-between;
  gap: 2rem;
  flex-wrap: wrap;
}

.ppam-info-card {
  margin: 1rem auto;
  padding: 20px;
  border-radius: 8px;
  flex: 1 1 45%;
  box-sizing: border-box;
  background-color: var(--text-hover);
}

.ppam-info-title {
  font-size: 1.5rem;
  color: var(--primary-color);
  margin-bottom: 1rem;
}

.ppam-info-description {
  font-size: 1rem;
  color: var(--primary-hover);
  text-align: justify;
}

@media (max-width: 800px) {
  .ppam-information {
    flex-direction: column;
  }

  .ppam-info-card {
    width: 100%;
    margin-bottom: 0;
  }
}

.ppam-images {
  width: 100%;
  display: flex;
  justify-content: center;
  gap: 1rem;
  flex-wrap: wrap;
  margin-top: 2rem;
}

.ppam-image-wrapper {
  flex: 1 1 300px;
  max-width: 90%;
  max-height: 400px;
  overflow: hidden;
  border-radius: 8px;
}

.ppam-image {
  width: 100%;
  height: 100%;
  object-fit: cover;
  border-radius: 8px;
}

@media (max-width: 800px) {
  .ppam-image-wrapper {
    flex: 1 1 100%;
  }

  .ppam-image {
    height: auto;
  }
}
</style>

