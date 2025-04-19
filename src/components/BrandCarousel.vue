<template>
  <section class="brand-carousel">
    <div class="brands">
      <img src="../assets/brand1.svg" alt="logo" class="base-img" />
      <img src="../assets/brand2.svg" alt="logo" class="base-img" />
      <img src="../assets/brand3.svg" alt="logo" class="base-img" />
      <img src="../assets/brand4.svg" alt="logo" class="base-img" />
      <img src="../assets/brand5.svg" alt="logo" class="base-img" />
      <img src="../assets/brand6.svg" alt="logo" class="base-img" />
      <img src="../assets/brand7.svg" alt="logo" class="base-img" />
    </div>
  </section>
</template>

<script setup>

</script>

<style scoped>
.brand-carousel {
  padding: 2rem 0;
}

.brands {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 2rem;
  flex-wrap: nowrap;
}

.base-img {
  height: 28px;
  width: 140px;

}

@media (max-width: 640px) {
  .brands {
    flex-wrap: wrap;
    gap: 1rem;
    justify-content: start;
  }

  .base-img {
    flex: 0 0 calc(50% - 0.5rem);
    width: auto;
    height: 1.5rem;
  }
}
</style>
