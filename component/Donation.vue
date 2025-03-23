<script setup>
const bankTransferSections = [
  {
    title: 'Donate via Bank Transfer',
    icon: 'i-heroicons-banknotes',
    content: 'Donate to PPA-M Account at MayBank – Account Number: 5640 6145 5054, Swift Code: MBBEMYKL'
  },
  {
    title: 'Send Us Your Transfer Slip',
    icon: 'i-heroicons-envelope',
    content: 'Kindly email us at info@ppam.my with your name and transfer slip so we can track your contribution.'
  },
  {
    title: 'Note on Tax Deduction',
    icon: 'i-heroicons-information-circle',
    content: 'PPA-M will issue a donation receipt to acknowledge your generosity.'
  },
  {
    title: 'Thank You!',
    icon: 'i-heroicons-heart',
    content: 'Thank you for being part of our mission to support Palestinian students in Malaysia.'
  }
]
</script>

<template>
  <section class="donate-section">
    <div class="donate-manual-container">
      <h2 class="title">Every Contribution Means the World to Us</h2>
      <h3 class="sub-title">
        Every Contribution Counts, Every Student Matters.
      </h3>
      <ul aria-label="Bank transfer instructions">
        <li v-for="(section, index) in bankTransferSections" :key="index">
          <UIcon
              :name="section.icon"
              class="icon"/>
          {{ section.content }}
        </li>
      </ul>
    </div>
  </section>
</template>

<style scoped>
.donate-section {
  display: flex;
  flex-direction: column;
  gap: 2rem;
  max-width: 1200px;
  margin: 3rem auto;
  padding: 0 1rem;
}

.donate-manual-container {
  background: #EEEEEE;
  padding: 2rem;
  box-shadow: rgba(149, 157, 165, 0.4) 3px 8px 24px;
}

.title {
  text-align: center;
  font-weight: bold;
  font-size: 1.5rem;
  color: var(--primary-color);
  margin-bottom: 1.5rem;
}

.sub-title {
  text-align: center;
  font-size: 1.1rem;
  color: var(--primary-hover);
  margin-bottom: 1.5rem;
}

.donate-manual-container ul {
  list-style: none;
  font-size: 1rem;
  width: 100%;
  max-width: 800px;
  margin: 0 auto 5rem auto;
}

.donate-manual-container ul li {
  display: flex;
  align-items: center;
  margin: 1rem 0;
  text-align: justify;
}

.donate-manual-container ul li .icon {
  margin-right: 1rem;
  font-size: 2rem;
  color: var(--primary-color);
}

.donate-manual-container a {
  color: var(--primary-color);
  text-decoration: underline;
  margin: 0 .5rem;
}

.donate-manual-container a:hover {
  text-decoration: none;
  transition: ease-in 0.3s;
}

@media (max-width: 768px) {
  .donate-section {
    padding: 0 0.5rem;
  }

  .donate-manual-container {
    padding: 1rem;
  }

  .title {
    font-size: 1.25rem;
  }

  .sub-title {
    font-size: 1rem;
  }
}
</style>