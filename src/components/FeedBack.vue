<!-- src/components/FeatureShare.vue -->
<template>
    <section class="feature-share">
   
      <div class="visual">
        <img src="../assets/feedback.svg" alt="API Illustration" />
      </div>
      <div class="content">
        <span class="badge">Feedback</span>
        <h1 class="title">Better feedback at the right time.</h1>
        <p class="description">
          Campsite has been instrumental in keeping designers aware of each others' work‑in‑progress in a way that was
          previously slowing us down. It’s also one of the only channels where...
        </p>
    
        <a href="#" class="cta">See how it works</a>
      </div>
  
    </section>
  </template>
  
  <script setup>
  // no JS needed right now
  </script>
  
  <style scoped>
  .feature-share {
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 150px;
    margin-top: 60px;
  }
  
  /* left side */
  .content {
    gap: 24px;
    width: 547px;
  }
  
  .badge {
    display: inline-block;
    background-color: #f25236;
    color: #fff;
    padding: 0.25rem 0.75rem;
    border-radius: 9999px;
    font-size: 14px;
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
  
  /* right side */
  
  
  .visual img {
    width: 358px;
    height: 361px;
  }
  
  /* Responsive */
  @media (max-width: 768px) {
    .feature-share {
      display: flex;
      flex-direction: column;
      align-items: center;    /* center panels */
      text-align: center;
      gap: 1.5rem;            /* vertical space between */
      margin-top: 40px;
      padding: 0 1rem;
    }
  
    .content {
      width: 100%;            /* fill the container */
      gap: 20px;
    }
  
    .visual {
      width: 100%;
      margin-top: 1rem;
      text-align: center;
    }
  
    .visual img {
      width: 100%;            /* scale to full width */
      height: auto;
      max-width: 600px;       /* optional cap */
    }
  }
  
  </style>