<template>
    <section class="testimonials-section">
      <div class="testimonials">
        <div class="testimonial">
          <img src="../assets/Layers1.svg" alt="Leaf Icon" class="icon" />
          <p class="testimonial-text">
            Cloudhub has emerged as an essential asset for the team at Patreon design. Amidst an accelerated
            expanding organization in which the product undergoes rapid changes, Campsite enables us to maintain
            visibility on what’s transpiring across various teams — impeccably aligning with our pre-existing procedures.
          </p>
          <div class="author">
            <img src="../assets/Avatar.svg" alt="Gabriel Valdivia" class="avatar" />
            <div class="author-info">
              <span class="author-name">Gabriel Valdivia</span>
              <span class="author-role">Principal Product Designer, Patreon</span>
            </div>
          </div>
        </div>
  
        <div class="testimonial">
          <img src="../assets/Layers2.svg" alt="Star Icon" class="icon" />
          <p class="testimonial-text">
            Cloudhub has demonstrated exceptional worth in preserving open communication among designers
            regarding their current endeavors, a challenge that previously impeded our progress. It continually
            stands as a distinctive platform guiding our dialogue towards imagination and consistent review,
            an element I highly value. Moreover, it has accelerated our propensity for early-stage feedback beyond
            my expectations.
          </p>
          <div class="author">
            <img src="../assets/Avatar2.svg" alt="Buzz Usborne" class="avatar" />
            <div class="author-info">
              <span class="author-name">Buzz Usborne</span>
              <span class="author-role">Principal Designer, Buildkite</span>
            </div>
          </div>
        </div>
      </div>
    </section>
  </template>
  
  <script setup>
  </script>
  
  <style scoped>
  .testimonials-section {
    width: 100%;
    background: #F9FAFB;
    padding: 4rem 1rem;
  }
  
  .testimonials {
    max-width: 1200px;
    margin: 0 auto;
    display: flex;
    gap: 2rem;
    justify-content: space-between;
  }
  
  .testimonial {
    flex: 0 1 calc(50% - 1rem);
    display: flex;

    flex-direction: column;
    padding: 2rem;
    border-radius: 0.75rem;
  }
  
  .icon {
    width: 2rem;
    height: 2rem;
  }
  
  .testimonial-text {
    margin-top: 1rem;
    color: #333;
    line-height: 1.5;
    flex-grow: 1;
  }
  
  .author {
    display: flex;
    align-items: center;
    margin-top: 1.5rem;
  }
  
  .avatar {
    width: 2.5rem;
    height: 2.5rem;
    border-radius: 50%;
    object-fit: cover;
  }
  
  .author-info {
    margin-left: 0.75rem;
  }
  
  .author-name {
    display: block;
    font-weight: 600;
    color: #111;
  }
  
  .author-role {
    display: block;
    font-size: 0.875rem;
    color: #666;
  }
  
  @media (max-width: 768px) {
    .testimonials {
      flex-direction: column;
      align-items: center;
    }
    .testimonial {
      flex: 0 1 100%;
      max-width: 540px;
    }
  }
  </style>
  