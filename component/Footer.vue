<script setup lang="ts">
const currentYear = new Date().getFullYear();
</script>

<template>
  <div class="footer">
    <div class="main-container">

      <div class="info-container">
        <div class="box">
          <span class="icon"><UIcon name="mdi-location"/></span>
          <p class="info">
            <a href="https://www.google.com/maps/place/Albukhary+International+University+(AIU)/@6.1336498,100.3863971,15z/data=!4m6!3m5!1s0x304b5ac489a998b9:0x3fa53e13f07fbb01!8m2!3d6.1336498!4d100.3863971!16s%2Fg%2F1216lnq4?entry=ttu&g_ep=EgoyMDI0MTAwOS4wIKXMDSoASAFQAw%3D%3D">
              Jalan Tun Abdul Razak,
              05200, Alor Setar,
              Kedah Darul Aman, Malaysia.
            </a>
          </p>
        </div>
        <div class="box">
          <span class="icon"><UIcon name="ic-baseline-phone"/></span>
          <p class="info"><a href="tel:+604774 7300">(60) 4774 7300</a></p>
        </div>
        <div class="box">
          <span class="icon"><UIcon name="ic-baseline-email"/></span>
          <p class="info"><a href="mailto:info@aiu.edu.my">info@aiu.edu.my</a></p>
        </div>
        <div class="box">
          <span class="icon"><UIcon name="mdi-university"/></span>
          <p class="info"><a href="https://aiu.edu.my/">Albukhary International University </a></p>
        </div>
      </div>
      <hr class="divider">

      <div class="socials-section">
        <div class="socials-container">
          <div></div>
          <div class="social-icons">
            <ul>
              <li>
                <a href="" target="_blank" rel="noopener">
                  <UIcon name="ic-baseline-facebook"/>
                </a>
              </li>
              <li>
                <a href="" target="_blank" rel="noopener">
                  <UIcon name="mdi-instagram"/>
                </a>
              </li>
            </ul>
          </div>
          <div></div>
        </div>
        <div class="footer-bottom">
          <p>&copy; Copyright <a href="http://www.ppam.my">Persatuan Progresif Malaysia – Palestin {{ currentYear }}</a>
          </p>
        </div>
      </div>

    </div>
  </div>
</template>

<style scoped lang="scss">
.footer {
  padding: 1em 0;
  background-color: var(--primary-color);
}

.main-container {
  display: block;
  padding: 0 100px;
}

@media (max-width: 800px) {
  .main-container {
    padding: 0;
  }
}

.info-container {
  display: flex;
  flex-direction: row;
}

.info-container div {
  flex: 25%;
}

.info-container div,
.links-container div {
  flex: 30%;
}

@media (max-width: 800px) {
  .info-container {
    display: block;
  }
}

.box {
  display: block;
  text-align: center;
  margin: 20px;
}

.box span {
  font-size: 3rem;
  color: var(--text-color);
}

.box > p {
  color: var(--text-color);
}

.divider {
  margin: 1rem 0;
  border: 2px solid var(--text-hover);
}

.links h2,
.subscribe-section h2,
.others-links-section h2 {
  color: var(--text-color);
  font-size: 1.5rem;
  margin: 15px 0;
}

.links ul li,
.others-links-section ul li {
  list-style: none;
  font-size: 1rem;
}

.links ul li a span,
.others-links-section li a span {
  color: var(--text-color);
  margin-right: .5rem;
}

.links ul li a,
.others-links-section li a {
  color: var(--text-color);
  margin-right: .5rem;
}

.links ul li a:hover,
.others-links-section li a:hover {
  color: var(--text-color);
  transition: .3s ease-in-out;
}

.socials-container {
  display: flex;
  justify-content: space-between;
}

.social-icons ul {
  display: flex;
  justify-content: space-between;
  gap: 0 10px;
  margin: 20px 0;
}

.social-icons ul li {
  width: 3rem;
  height: 3rem;
  text-align: center;
  font-size: 1.5rem;
  padding: 5px;
  border: 2px solid var(--text-color);
  border-radius: 50%;
  color: var(--text-color);
}

.social-icons ul li:hover {
  color: var(--text-hover);
  border: 2px solid var(--text-hover);
  transition: .3s ease-in-out;
}

@media (max-width: 1200px) {
  .links ul li span {
    display: none;
  }

  .others-links-section ul li span {
    display: none;
  }
}

.footer-bottom {
  text-align: start;
  font-size: 1.2rem;
  color: var(--text-color);
  padding: 2rem 0;
}

.footer-bottom a {
  color: var(--text-color);
}

a:hover {
  color: var(--text-hover);
}

.info {
  a {
    text-decoration: none;
  }
}
</style>
