<template>
  <footer class="footer-section">
    <div class="footer-inner">
   
      <div class="footer-columns">
        <div class="footer-logo">
        <img src="../assets/logodemo.svg" alt="DejectStudio Logo" />
      </div>
        <div class="footer-column">
          <h4>Product</h4>
          <ul>
            <li><a href="#">Features</a></li>
            <li><a href="#">Pricing</a></li>
            <li><a href="#">Changelog</a></li>
            <li><a href="#">Support</a></li>
          </ul>
        </div>
        <div class="footer-column">
          <h4>Legal</h4>
          <ul>
            <li><a href="#">Terms of Privacy</a></li>
            <li><a href="#">Privacy Policy</a></li>
            <li><a href="#">Security</a></li>
          </ul>
        </div>
        <div class="footer-column">
          <h4>Company</h4>
          <ul>
            <li><a href="#">Blog</a></li>
            <li><a href="#">Contact</a></li>
          </ul>
        </div>
        <div class="footer-column">
          <h4>Social</h4>
          <ul>
            <li><a href="#">Dribbble</a></li>
            <li><a href="#">Behance</a></li>
            <li><a href="#">Discord</a></li>
          </ul>
        </div>
      </div>
    </div>
    <div class="footer-bottom">
      All rights reserved.© 2024 DejectStudio
    </div>
  </footer>
</template>

<script setup>
</script>

<style scoped>
.footer-section {
  width: 100%;
  background: #fff;
  color: #333;
  padding: 2rem 1rem;
}

.footer-inner {
  max-width: 1200px;
  margin: 0 auto;
  display: flex;
  align-items: flex-start;
  justify-content: space-between;
  gap: 2rem;
}

.footer-logo img {
  width: 40px;
  height: 40px;
  margin-top: 20px;
  
}

.footer-columns {
  display: flex;
  flex: 1;
  gap: 140px;
}

.footer-column {
  min-width: 120px;
}

.footer-column h4 {
  margin-bottom: 0.5rem;
  font-size: 1rem;
  font-weight: 600;
  color: #111;
}

.footer-column ul {
  list-style: none;
  padding: 0;
  margin: 0;
}

.footer-column li {
  margin-bottom: 0.5rem;
}

.footer-column a {
  color: #555;
  text-decoration: none;
  font-size: 0.875rem;
}

.footer-column a:hover {
  color: #000;
}

.footer-bottom {
  max-width: 1200px;
  margin: 1.5rem auto 0;
  text-align: center;
  font-size: 0.75rem;
  color: #999;
}

@media (max-width: 768px) {
  .footer-inner {
    flex-direction: column;
    align-items: center;
    text-align: center;
  }
  .footer-columns {
    flex-direction: column;
    gap: 1.5rem;
    width: 100%;
  }
  .footer-column {
    min-width: 100%;
  }
}
</style>
