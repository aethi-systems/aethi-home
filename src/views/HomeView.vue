<script setup>
import logoUrl from '@/assets/aethi-black.png'
</script>

<template>
  <main>
    <!-- Hero -->
    <section class="hero">
      <div class="wrapper hero__inner">
        <img class="hero__logo" :src="logoUrl" alt="aethi" />

        <h1 class="hero__title">Engineering. Data. Systems.</h1>
        <p class="hero__tagline muted">
          A boutique technology firm delivering institution-grade platforms—quietly, precisely, reliably.
        </p>

        <div class="hero__cta">
          <a class="button" href="mailto:contact@aethi.co.uk" aria-label="Contact aethi">Contact</a>
        </div>

        <!-- Subtle trust markers (optional) -->
        <ul class="hero__pills" aria-label="Focus areas">
          <li>World-data platforms</li>
          <li>Low-latency systems</li>
          <li>Data lineage & quality</li>
          <li>Security by design</li>
        </ul>
      </div>
    </section>

    <!-- Value props -->
    <section class="section">
      <div class="wrapper grid">
        <article class="card">
          <h3>Financial-grade software</h3>
          <p class="subtle">
            Systems engineered for determinism, auditability and scale—built with the same care expected in global markets.
          </p>
        </article>

        <article class="card">
          <h3>World data, without friction</h3>
          <p class="subtle">
            Vendor integrations, lineage, entitlements and quality controls.
          </p>
        </article>

        <article class="card">
          <h3>Architecture that lasts</h3>
          <p class="subtle">
            Clear boundaries, resilient paths-to-operate, and automation from day one. Less noise, more signal.
          </p>
        </article>

        <article class="card">
          <h3>Security, quietly enforced</h3>
          <p class="subtle">
            Principles, not checklists: least privilege, clean secrets, verified builds, and observability where it matters.
          </p>
        </article>
      </div>
    </section>

    <!-- Statement -->
    <section class="section">
      <div class="wrapper statement">
        <p>
          We’re not here to advertise. We’re here to deliver.
          Fewer slides, more substance. If you know, you know.
        </p>
      </div>
    </section>
  </main>
</template>

<style scoped>
.hero__inner {
  display: grid;
  place-items: center;
  text-align: center;
  gap: 0.25rem;
}

.hero__logo {
  height: clamp(64px, 10vw, 120px);
  width: auto;
  margin-bottom: 0.25rem;
}

.hero__title {
  font-size: clamp(1.6rem, 3.5vw, 2.6rem);
  letter-spacing: 0.01em;
  line-height: 1.15;
}

.hero__tagline {
  max-width: 60ch;
}

.hero__cta {
  display: flex;
  gap: 0.75rem;
  margin-top: 0.5rem;
  flex-wrap: wrap;
  justify-content: center;
}

.hero__pills {
  display: flex;
  gap: 0.5rem;
  margin-top: 1rem;
  padding: 0;
  list-style: none;
  flex-wrap: wrap;
  justify-content: center;
}

.hero__pills li {
  border-radius: 999px;
  padding: 0.35rem 0.7rem;
  font-size: 0.95rem;
  white-space: nowrap;
}

.grid {
  display: grid;
  gap: 1rem;
  grid-template-columns: repeat(12, 1fr);
}

.grid > .card {
  grid-column: span 12;
}

@media (min-width: 720px) {
  .grid > .card { grid-column: span 6; }
}

@media (min-width: 1024px) {
  .grid > .card { grid-column: span 3; }
}

.statement {
  text-align: center;
  font-size: clamp(1.05rem, 1.2vw, 1.25rem);
  color: rgba(255,255,255,0.78);
}
</style>
