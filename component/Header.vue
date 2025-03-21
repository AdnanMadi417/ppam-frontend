<script setup>

</script>

<template>
  <div class="header-container">
    <div class="header-wrapper">
      <div class="logo-container">
        <div class="logo">
          <a href="http://www.ppam.my">
            <img src="/images/ppam-logo.png" alt="PPAM Logo" />
          </a>
        </div>
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
  max-height: 500px;
}

.header-wrapper {
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
  align-items: center;
}

.logo img {
  width: 90px;
  height: 70px;
}

.header-title h2 {
  font-size: 1.5rem;
  font-weight: normal;
  text-transform: uppercase;
  color: var(--primary-color);
}

@media (max-width: 1200px) {
  .header-wrapper {
    display: block;
  }

  .logo-container {
    display: flex;
    justify-content: space-between;
  }

}
</style>
