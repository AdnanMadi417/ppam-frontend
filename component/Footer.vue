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
            <a href="https://www.google.com/maps/place/Palestinian+Progressive+Association+Malaysia/@3.2000926,101.714227,17z/data=!3m1!4b1!4m6!3m5!1s0x31cc3973161d5f85:0xb2a9f84a181acb11!8m2!3d3.2000872!4d101.7168019!16s%2Fg%2F11jkq14vh2?entry=ttu&g_ep=EgoyMDI1MDMxOS4xIKXMDSoASAFQAw%3D%3D">
              Jalan Genting Kelang, Taman Danau Kota, 53100 Kuala Lumpur, Wilayah Persekutuan Kuala Lumpur
            </a>
          </p>
        </div>
        <div class="box">
          <span class="icon"><UIcon name="ic-baseline-phone"/></span>
          <p class="info"><a href="tel:+60341444240">(60) 3414 44240</a></p>
        </div>
        <div class="box">
          <span class="icon"><UIcon name="ic-baseline-email"/></span>
          <p class="info"><a href="mailto:info@ppam.my">info@ppam.my</a></p>
        </div>
        <div class="box">
          <span class="icon"><UIcon name="mdi-university"/></span>
          <p class="info">
            <a
                href="http://ppam.my">
              Empowering Students, Strengthening Palestine
            </a>
          </P>
        </div>
      </div>
      <hr class="divider">

      <div class="socials-section">
        <div class="socials-container">
          <div></div>
          <div class="social-icons">
            <ul>
              <li>
                <a href="https://www.facebook.com/ppa.my.pal?mibextid=LQQJ4d" target="_blank" rel="noopener">
                  <UIcon name="ic-baseline-facebook"/>
                </a>
              </li>
              <li>
                <a href="https://www.instagram.com/ppa.my.pal?igsh=b2h1dTM4YzN2M3Ni" target="_blank" rel="noopener">
                  <UIcon name="mdi-instagram"/>
                </a>
              </li>
            </ul>
          </div>
          <div></div>
        </div>
        <div class="footer-bottom">
          <p>&copy; All Copyright Reserved For <a href="http://ppam.my">Palestinian Progressive Association- Malaysia
            {{ currentYear }}</a>
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
  list-style: none;
  width: 3rem;
  height: 3rem;
  text-align: center;
  font-size: 1.5rem;
  padding: 8px;
  border: 2px solid var(--text-color);
  border-radius: 50%;
}

.social-icons ul li a {
  color: var(--text-color);
  align-items: center;
  text-align: center;
  text-decoration: none;
}

.social-icons ul li:hover {
  color: var(--text-hover);
  border: 2px solid var(--text-hover);
  transition: .3s ease-in-out;
}

.social-icons ul li a {
  color: var(--text-hover);
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
  text-decoration: none;
  transition: color 0.3s ease-in-out;
}

.footer-bottom a:hover {
  color: var(--text-hover);
  text-decoration: underline;
}

.info a {
  text-decoration: none;
  color: var(--text-color);
  transition: color 0.3s ease-in-out;
}

.info a:hover {
  color: var(--text-hover);
}

@media (max-width: 768px) {
  .footer-bottom {
    font-size: 1rem;
    padding: 1.5rem 1rem;
    text-align: center;
  }
}

@media (max-width: 480px) {
  .footer-bottom {
    font-size: 0.9rem;
    padding: 1rem 0.5rem;
    text-align: center;
  }

  .footer-bottom a,
  .info a {
    word-break: break-word;
    font-size: 0.95rem;
  }
}


</style>
