<script setup>
import { ref } from 'vue'

const isSidebarOpen = ref(false)
const dropdownStates = ref({})

const toggleDropdown = (name) => {
  dropdownStates.value[name] = !dropdownStates.value[name]
}

const navLinks = [
  {
    name: 'Product',
    href: '#',
    hasDropdown: true,
    children: [
      { name: 'Feature 1', href: '#' },
      { name: 'Feature 2', href: '#' },
    ],
  },
  { name: 'Home', href: 'home' },
  { name: 'Shop', href: 'shop' },
  { name: 'Pages', href: 'pages' },
  { name: 'Integrations', href: 'integrations' },
  { name: 'Developers', href: 'developers' },
]
</script>

<template>
  <header class="header">
    <nav class="nav-container">
      <div class="logo-area">
        <img src="../assets/logoo.svg" alt="logo" class="logo-img" />

        <ul class="nav-links">
          <li v-for="link in navLinks" :key="link.name" class="nav-item" :class="{ 'has-dropdown': link.hasDropdown }">
            <a :href="link.href">
              {{ link.name }}
              <svg v-if="link.hasDropdown" xmlns="http://www.w3.org/2000/svg" class="chevron-icon" width="16"
                height="16" fill="currentColor" viewBox="0 0 20 20">
                <path fill-rule="evenodd"
                  d="M5.23 7.21a.75.75 0 011.06.02L10 11.293l3.71-4.06a.75.75 0 111.08 1.04l-4.25 4.657a.75.75 0 01-1.08 0L5.25 8.27a.75.75 0 01-.02-1.06z"
                  clip-rule="evenodd" />
              </svg>
            </a>
            <ul v-if="link.hasDropdown" class="dropdown">
              <li v-for="sublink in link.children" :key="sublink.name">
                <a :href="sublink.href">{{ sublink.name }}</a>
              </li>
            </ul>
          </li>
        </ul>
      </div>

      <div class="auth desktop-only">
        <a href="#" class="login-link">Login</a>
        <a href="#" class="btn-primary">Start for free</a>
      </div>

      <button class="menu-btn mobile-only" @click="isSidebarOpen = true">
        <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" fill="currentColor" viewBox="0 0 24 24">
          <path d="M4 6h16M4 12h16M4 18h16" stroke="#000" stroke-width="2" stroke-linecap="round" />
        </svg>
      </button>
    </nav>

    <div class="sidebar" v-if="isSidebarOpen">
      <button class="close-btn" @click="isSidebarOpen = false">×</button>
      <ul class="sidebar-links">
        <li v-for="link in navLinks" :key="link.name">
          <div @click="link.hasDropdown ? toggleDropdown(link.name) : isSidebarOpen = false" class="sidebar-link">
            {{ link.name }}
            <span v-if="link.hasDropdown" class="dropdown-toggle-icon">▾</span>
          </div>
          <ul v-if="link.hasDropdown && dropdownStates[link.name]" class="mobile-dropdown">
            <li v-for="sublink in link.children" :key="sublink.name">
              <a :href="sublink.href" @click="isSidebarOpen = false">{{ sublink.name }}</a>
            </li>
          </ul>
        </li>
      </ul>
    </div>
  </header>
</template>

<style scoped>
@import url("https://rsms.me/inter/inter.css");

:root {
  --brand: #ff5225;
  --text: #000;
}

* {
  box-sizing: border-box;
}

a {
  text-decoration: none;
  color: inherit;
}

ul {
  list-style: none;
  padding: 0;
  margin: 0;
}

.header {
  font-family: "Inter", sans-serif;
}

.nav-container {
  max-width: 1280px;
  margin: auto;
  padding: 1rem 1.5rem;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.logo-area {
  display: flex;
  align-items: center;
  gap: 120px;
}

.logo-img {
  height: 25px;
}

.nav-links {
  display: none;
  gap: 20px;
  font-size: 14px;
  font-weight: 500;
}

@media (min-width: 1024px) {
  .nav-links {
    display: flex;
  }
}

.nav-links li a {
  display: flex;
  align-items: center;
  gap: 4px;
  padding: 0.5rem;
}


.has-dropdown {
  position: relative;
}

.has-dropdown .dropdown {
  display: none;
  position: absolute;
  top: 100%;
  left: 0;
  background: white;
  padding: 0.75rem;
  border-radius: 0.25rem;
  box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.08);
  z-index: 10;
  min-width: 140px;
}

.has-dropdown:hover .dropdown {
  display: block;
}

.dropdown li {
  padding: 0.25rem 0;
}

.dropdown li a {
  font-size: 14px;
  font-weight: 400;
  display: block;
  color: #333;
}

.chevron-icon {
  margin-left: 4px;
}

/* Auth */
.auth {
  display: flex;
  gap: 1rem;
  align-items: center;
  font-size: 14px;
}

.btn-primary {
  padding: 0.5rem 1.25rem;
  border-radius: 9999px;
  background: #ff663f;
  color: #fff;
  font-weight: 600;
  box-shadow: 0 3px 10px rgba(0, 0, 0, 0.15);
}

.login-link {
  display: inline-block;
}

.menu-btn {
  background: none;
  border: none;
  cursor: pointer;
  padding: 0.5rem;
}

/* Desktop only */
.desktop-only {
  display: none;
}

@media (min-width: 1024px) {
  .desktop-only {
    display: flex;
  }

  .mobile-only {
    display: none;
  }
}

/* Sidebar for mobile */
.sidebar {
  position: fixed;
  top: 0;
  right: 0;
  width: 240px;
  height: 100vh;
  background-color: white;
  padding: 2rem 1rem;
  box-shadow: -2px 0 10px rgba(0, 0, 0, 0.1);
  z-index: 50;
  display: flex;
  flex-direction: column;
  gap: 1rem;
}

.close-btn {
  align-self: flex-end;
  font-size: 2rem;
  background: none;
  border: none;
  cursor: pointer;
}

.sidebar-links li {
  margin-top: 1rem;
}

.sidebar-link {
  display: flex;
  justify-content: space-between;
  align-items: center;
  cursor: pointer;
  padding: 0.5rem 0;
  font-weight: 500;
}

.dropdown-toggle-icon {
  font-size: 1rem;
  margin-left: 8px;
}

.mobile-dropdown {
  margin-left: 1rem;
  margin-top: 0.25rem;
}
</style>
