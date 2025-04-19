<template>
  <section class="loved-by-section">
    <h2 class="section-title">Loved By Designers At</h2>
    <div class="logo-grid">
      <div class="logo-item">
        <img src="../assets/design1.svg" alt="CrowdStrike" />
      </div>
      <div class="logo-item">
        <img src="../assets/design2.svg" alt="CrowdStrike" />
      </div>
      <div class="logo-item">
        <img src="../assets/design3.svg" alt="CrowdStrike" />
      </div>
      <div class="logo-item">
        <img src="../assets/design4.svg" alt="CrowdStrike" />
      </div>
      <div class="logo-item">
        <img src="../assets/design5.svg" alt="CrowdStrike" />
      </div>
      <div class="logo-item">
        <img src="../assets/design6.svg" alt="CrowdStrike" />
      </div>
      <div class="logo-item">
        <img src="../assets/design7.svg" alt="CrowdStrike" />
      </div>
      <div class="logo-item">
        <img src="../assets/design8.svg" alt="CrowdStrike" />
      </div>
    </div>
  </section>
</template>

<script setup>

</script>

<style scoped>
.loved-by-section {
  max-width: 1200px;
  margin: 0 auto;
  padding: 4rem 1rem;
  text-align: center;
}

.section-title {
  font-size: 2rem;
  font-weight: 600;
  color: #333;
  margin-bottom: 2rem;
}

.logo-grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 32px 24px;
  justify-content: center;
}

.logo-item {
  background: #f9f9f9;
  width: 296px;
  height: 144px;
  border-radius: 24px;
  display: flex;
  align-items: center;
  justify-content: center;
}

.logo-item img {
  max-width: 70%;       
  max-height: 70%;
  object-fit: contain;
}

@media (max-width: 768px) {
  .logo-grid {
    grid-template-columns: repeat(2, 1fr);
    gap: 16px;
  }
  .logo-item {
    width: 100%;
    max-width: 296px;
    height: 144px;
  }
}
</style>
