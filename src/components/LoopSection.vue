<template>
    <section class="loop-section">
      <div class="loop-inner">
        <h2 class="loop-title">Keep every one in the loop</h2>
        <p class="loop-subtitle">All good things start with a homepage. Get inspired without breaking your wallet.</p>
        <button class="loop-cta">Start for free</button>
        <div class="loop-visual">
          <img src="../assets/dashboard.svg" alt="Project dashboard screenshot" />
        </div>
      </div>
    </section>
  </template>
  
  <script setup>
  </script>
  
  <style scoped>
  .loop-section {
    position: relative;
    left: 50%;
    right: 50%;
    width: 100vw;
    margin-left: -50vw;
    margin-right: -50vw;
    background: linear-gradient(135deg, #ff5722, #ff7043);
    padding: 4rem 0;
    color: #fff;
    box-sizing: border-box;
    margin-top: 60px;
  }
  
  .loop-inner {
    max-width: 1000px;
    margin: 0 auto;
    display: flex;
    flex-direction: column;
    align-items: center;
  }
  
  .loop-title {
    font-size: 2.5rem;
    font-weight: 700;
    margin-bottom: 1rem;
  }
  
  .loop-subtitle {
    font-size: 1rem;
    margin-bottom: 2rem;
    opacity: 0.9;
  }
  
  .loop-cta {
    background: #fff;
    color: #ff5722;
    border: none;
    padding: 0.75rem 2rem;
    border-radius: 9999px;
    font-size: 1rem;
    font-weight: 600;
    cursor: pointer;
    margin-bottom: 3rem;
  }
  
  .loop-visual {
    margin-top: auto;
    margin-bottom:-64px; 
    width: 100%;
    display: flex;
    justify-content: center;
  }
  
  .loop-visual img {
    width: 100%;
    max-width: 900px;
    height: auto;
    border-radius: 0.5rem;
    box-shadow: 0 8px 24px rgba(0,0,0,0.2);
  }
  
  /* Responsive */
  @media (max-width: 768px) {
    .loop-title {
      font-size: 2rem;
    }
    .loop-subtitle {
      font-size: 0.9rem;
    }
    .loop-cta {
      padding: 0.75rem 1.5rem;
      font-size: 0.9rem;
      margin-bottom: 2rem;
    }
  }
  </style>
  