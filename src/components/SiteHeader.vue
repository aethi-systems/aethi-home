<template>
  <header class="site-header">
    <div class="header-left">
      <RouterLink to="/" class="brand-link" aria-label="Aethi home">
        <img class="logo" :src="logoUrl" alt="Aethi" />
        <span class="brand">aethi</span>
      </RouterLink>
    </div>

    <nav class="primary-nav" aria-label="Primary">
      <RouterLink to="/" class="nav-link">Home</RouterLink>
      <RouterLink to="/about" class="nav-link">About</RouterLink>
      <!-- <RouterLink to="/services" class="nav-link">Services</RouterLink> -->
      <!-- <RouterLink to="/contact" class="nav-link">Contact</RouterLink> -->
    </nav>
  </header>
</template>

<script setup>
import { RouterLink } from 'vue-router'
import logoUrl from '@/assets/aethi-icon.png'
</script>

<style scoped>
.site-header {
  position: sticky;
  top: 0;
  z-index: 40;
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 1rem;

  padding: 0.75rem 1.25rem;
  background: var(--aethi-bg);
  color: var(--aethi-fg);
  border-bottom: 1px solid rgba(255,255,255,0.08);
}

.header-left {
  display: flex;
  align-items: center;
}

.brand-link {
  display: inline-flex;
  align-items: center;
  gap: 0.75rem;
  text-decoration: none;
  color: inherit;
}

.logo {
  /* Bigger logo with responsive clamp */
  height: clamp(22px, 6vw, 36px);
  width: auto;
  display: block;
}

.brand {
  font-size: clamp(1.1rem, 2vw, 1.35rem);
  letter-spacing: 0.02em;
  margin: 0;
}

.primary-nav {
  display: flex;
  align-items: center;
  gap: 1rem;
  white-space: nowrap;   /* keep links on one line */
}

/* Make room for the underline inside the link box */
.nav-link {
  position: relative;
  padding: 0.5rem 0.1rem 0.6rem; /* extra bottom space */
  text-decoration: none;
  color: rgba(255,255,255,0.88);
  font-weight: 500;
}

/* Draw the underline inside the link box */
.router-link-active.nav-link::after,
.router-link-exact-active.nav-link::after {
  content: "";
  position: absolute;
  left: 0;
  right: 0;
  bottom: 0;
  height: 2px;
  border-radius: 2px;
  background: #fff;
  opacity: 0.9;
}

/* Small screens: tighten spacing a bit */
@media (max-width: 420px) {
  .primary-nav { gap: 0.75rem; }
}
</style>
