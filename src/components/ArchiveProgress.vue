<!-- src/components/ArchiveProgress.vue -->
<template>
    <section class="archive-section">
      <div class="archive-inner">
        <h2 class="archive-title">Your Archive of progress</h2>
        <div class="archive-cards">
          <!-- Card: Projects -->
          <div class="card">
            <div class="card-header">
              <h3>Projects</h3>
              <p>Organize, follow, and archive.</p>
            </div>
            <div class="card-content">
              <img src="../assets/Group.svg" alt="Projects Overview Chart" />
            </div>
          </div>
    
          <!-- Card: Member profiles -->
          <div class="card">
            <div class="card-header">
              <h3>Member profiles</h3>
              <p>Automatic portfolios of your work.</p>
            </div>
            <div class="card-content">
              <img src="../assets/Group1.svg" alt="Member Profiles Chart" />
            </div>
          </div>
        </div>
      </div>
    </section>
  </template>
  
  <script setup>
  // no JS needed
  </script>
  
  <style scoped>
  /* full-width section with background */
  .archive-section {
    width: 100%;
    background: #fafafa;
    padding: 4rem 0;
  }
  
  /* center & constrain content */
  .archive-inner {
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 1rem;
    text-align: center;
  }
  
  .archive-title {
    font-size: 2rem;
    font-weight: 600;
    color: #333;
    margin-bottom: 2rem;
  }
  
  /* layout for two cards */
  .archive-cards {
    display: flex;
    justify-content: space-between;
    gap: 2rem;
    flex-wrap: wrap;
  }
  
  /* each card is a vertical flex container */
  .card {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    flex: 0 1 calc(50% - 1rem);
    background: #f9f9f9;
    border-radius: 0.75rem;
    box-shadow: 0 4px 16px rgba(0,0,0,0.05);
    overflow: hidden;
  }
  
  /* header centered */
  .card-header {
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 1.5rem;
   
  }
  
  .card-header h3 {
    margin: 0;
    font-size: 1.25rem;
    color: #111;
  }
  
  .card-header p {
    margin: 0.25rem 0 0;
    font-size: 0.875rem;
    color: #666;
  }
  
  /* content sits at bottom */
  .card-content {
    margin-top: auto;
    padding: 1rem;
    text-align: center;
  }
  
  .card-content img {
    width: 100%;
    height: auto;
    border-radius: 0.5rem;
  }
  
  /* responsive stacking */
  @media (max-width: 768px) {
  .archive-cards {
    flex-direction: column;
    align-items: center;    /* center cards */
    gap: 1.5rem;
  }
  .card {
    flex: none;
    width: 90%;             /* narrower width */
    max-width: 540px;
  }
}
  </style>
  