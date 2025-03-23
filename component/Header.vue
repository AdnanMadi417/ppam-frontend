<script setup>

const logo = "./images/ppam-header-logo.png"

</script>

<template>
  <div class="header-container">
    <div class="header-wrapper">

      <div class="logo-container">
        <a href="http://ppam.my">
          <img :src="logo" alt="PPAM Logo"/>
        </a>
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

@media (max-width: 992px) {
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
}

@media (max-width: 480px) {
  .logo-container img {
    width: 60px;
  }
}
</style>
