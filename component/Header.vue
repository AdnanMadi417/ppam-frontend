<script setup>

</script>

<template>
  <div class="header-container">
    <div class="header-wrapper">

      <div class="logo-container">
        <a href="http://www.ppam.my">
          <img src="~/images/ppam-logo.png" alt="PPAM Logo"/>
        </a>
      </div>

      <div class="header-title">
        <h2>Persatuan Progresif Malaysia – Palestin</h2>
      </div>

    </div>
  </div>
</template>

<style scoped>
.header-container {
  background-color: var(--primary-color);
  padding: 0.5rem 1rem;
}

.header-wrapper {
  display: flex;
  justify-content: space-between;
  align-items: center;
  flex-wrap: wrap;
}

.logo-container img {
  width: 90px;
  height: auto;
}

.header-title h2 {
  font-size: 1.8rem;
  font-weight: normal;
  text-transform: uppercase;
  color: var(--text-color);
  text-align: center;
}

@media (max-width: 992px) {
  .header-title h2 {
    font-size: 1.4rem;
  }

  .header-wrapper {
    justify-content: center;
    text-align: center;
  }

  .logo-container img {
    width: 80px;
  }
}

@media (max-width: 768px) {
  .header-wrapper {
    display: flex;
    justify-content: space-between;
    align-items: center;
    text-align: center;
  }

  .logo-container img {
    width: 70px;
  }

  .header-title h2 {
    font-size: 1.2rem;
  }
}

@media (max-width: 480px) {
  .header-title h2 {
    font-size: 1rem;
  }

  .logo-container img {
    width: 60px;
  }
}
</style>
