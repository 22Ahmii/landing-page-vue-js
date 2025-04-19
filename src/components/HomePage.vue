<!-- HeroSection.vue -->
<template>
  <section class="hero">
    <!-- headline block -->
    <div class="copy">
      <h1>Create, inspect, and apply<br />synthetic surveillance broadly.</h1>
      <p class="sub">Start with a stunning homepage. Stay motivated without hurting your pocket.</p>
      <div class="cta-row">
        <button class="cta">Start for free</button>
        <a href="#" class="demo">Want to talk or get a live demo? <span>Get in touch →</span></a>
        <div class="image-stack">
    <img src="../assets/frame1.svg" alt="logo" class="base-img" />
    <img src="../assets/frame3.svg" alt="logo" class="overlay-img" />
  </div>
      </div>
    </div>
  </section>
</template>

<script setup>

</script>

<style scoped>
.image-stack {
  margin-top:-320px;
  position: relative;
  width: fit-content;
}

.base-img {
  display: block;
  width: 100%;
  height: auto;
}

.overlay-img {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%; /* Match base-img */
  height: auto;
  transform: translate(10px, 10px); /* Default desktop offset */
}

/* Mobile responsiveness */
@media (max-width: 768px) {
  .image-stack {
    margin-top: 1rem;
    width: 100%;
    max-width: 320px;
  }

  .base-img,
  .overlay-img {
    width: 100%;
  }

  .overlay-img {
    transform: translate(5px, 5px); /* Slight shift for mobile */
  }
}

/* layout */
.hero {
  position: relative;
  overflow: hidden;
  padding: 6rem 1rem 10rem;
  text-align: center;
  background: #fff;
  isolation: isolate;     
}

.copy h1 {
  font-size: clamp(2.2rem, 6vw, 4rem);
  line-height: 1.1;
  font-weight: 600;
  margin: 0 0 1rem;
}

.copy .sub {
  max-width: 40rem;
  margin: 0 auto 2.5rem;
  color: #666;
}

.cta-row {
  display: flex;
  flex-direction: column;
  gap: 1rem;
  align-items: center;
}

.cta {
  background: #ff5630;
  color: #fff;
  font-weight: 600;
  border: 0;
  padding: .9rem 2.2rem;
  border-radius: 999px;
  cursor: pointer;
  transition: transform .2s ease;
}
.cta:hover { transform: translateY(-2px); }

.demo {
  font-size: .9rem;
  color: #444;
  text-decoration: none;
}
.demo span { font-weight: 600; }

/* svg rays */
.rays {
  position: absolute;
  bottom: -2rem;
  left: 50%;
  width: 150%;
  height: 50rem;
  transform: translateX(-50%);
  pointer-events: none;
}

/* center cube */
.center-icon {
  position: absolute;
  left: 50%;
  bottom: calc(4rem + 64px);      /* just above the bottom edge */
  transform: translateX(-50%);
  width: 64px;
  height: 64px;
  border-radius: 16px;
  background: #ff5630;
  display: flex;
  align-items: center;
  justify-content: center;
  z-index: 2;
}
.center-icon img { width: 50%; height: 50%; }

/* peripheral app icons */
.app-icon {
  position: absolute;
  width: 48px;
  height: 48px;
  border-radius: 12px;
  display: grid;
  place-items: center;
  background: white;
  box-shadow: 0 3px 10px rgba(0,0,0,.08);
}
.app-icon img { width: 80%; height: 80%; object-fit: cover; }
</style>