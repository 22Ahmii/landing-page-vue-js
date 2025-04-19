<template>
  <section class="feature-share">
    <div class="content">
      <span class="badge">Share</span>
      <h1 class="title">Share anything you’re working on.</h1>
      <p class="description">
        Campsite has been instrumental in keeping designers aware of each others' work‑in‑progress in a way that was
        previously slowing us down. It’s also one of the only channels where...
      </p>
      <ul class="highlights">
        <li>Coded</li>
        <li>100% Secure</li>
      </ul>
      <a href="#" class="cta">See how it works</a>
    </div>

    <div class="visual">
      <img src="../assets/api.svg" alt="API Illustration" />
    </div>
  </section>
</template>

<script setup>

</script>

<style scoped>
.feature-share {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 150px;
  margin-top: 60px;
}

.content {
  gap: 40px;
  width: 547px;
}

.badge {
  display: inline-block;
  background-color: #f25236;
  color: #fff;
  padding: 0.25rem 0.75rem;
  border-radius: 9999px;
  font-size: 0.875rem;
  font-weight: 600;
}

.title {
  margin-top: 0.75rem;
  font-size: 51px;
  line-height: 1.2;
  font-weight: 700;
  color: #111;
}

.description {
  margin-top: 1rem;
  color: #555;
  line-height: 1.5;
}

.highlights {
  display: flex;
  gap: 1.5rem;
  margin-top: 1rem;
  list-style: none;
  padding: 0;
}

.highlights li {
  position: relative;
  padding-left: 1.75rem;
}

.highlights li::before {
  content: '✔︎';
  position: absolute;
  left: 0;
  top: 50%;
  transform: translateY(-50%);
  width: 0.95rem;
  height: 0.95rem;
  border-radius: 50%;
  background: rgb(241, 231, 231);
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 0.6rem;
  color: black;
}

.cta {
  display: inline-block;
  margin-top: 1.5rem;
  color: #f25236;
  text-decoration: none;
  font-weight: 600;
  position: relative;
  padding-left: 1.25rem;
}

.cta::before {
  content: '▶';
  position: absolute;
  left: 0;
  top: 0;
  font-size: 0.9rem;
}

.visual img {
  max-width: 531px;
  height: 337px;
}

@media (max-width: 768px) {
  .feature-share {
    display: flex;
    flex-direction: column;
    align-items: center;
    text-align: center;
    gap: 1.5rem;
    margin-top: 40px;
    padding: 0 1rem;
  }

  .content {
    width: 100%;
    gap: 20px;
  }

  .visual {
    width: 100%;
    margin-top: 1rem;
    text-align: center;
  }

  .visual img {
    width: 100%;
    height: auto;
    max-width: 600px;
  }
}
</style>