<script setup>
import logoUrl from '@/assets/aethi-black.png'
</script>

<template>
  <main>
    <section class="hero">
      <div class="wrapper hero__about">
        <h1 class="hero__title">About aethi</h1>
        <p class="hero__tagline muted">
          We build institution-grade platforms for teams that value precision, security, and longevity.
        </p>
      </div>
    </section>

    <!-- What we do -->
    <section class="section">
      <div class="wrapper grid">
        <article class="card">
          <h2>What we do</h2>
          <p class="subtle">
            Bringing experience across private, public, and financial sectors—with security by design—to deliver scalable, powerful, bespoke systems, engineered for clarity and simplicity.
          </p>
        </article>

        <article class="card">
          <h2>How we work</h2>
          <ul class="list">
            <li><strong>Deterministic engineering:</strong> auditability, reproducibility, and measured performance.</li>
            <li><strong>Architecture first:</strong> clear boundaries, stable contracts, pragmatic automation.</li>
            <li><strong>Operate from day one:</strong> observability, SLOs, runbooks, and minimal toil.</li>
            <li><strong>Security woven in:</strong> least privilege, clean secrets, verified builds.</li>
          </ul>
        </article>

        <article class="card">
          <h2>Engagement</h2>
          <p class="subtle">
            Small footprint and a high bar. Scope quickly and deliver quietly.
          </p>
          <div class="cta-row">
            <a class="button" href="mailto:contact@aethi.co.uk" aria-label="Contact aethi">Start a conversation</a>
          </div>
        </article>
      </div>
    </section>

    <section class="section">
      <div class="wrapper statement">
        <p>Fewer slides. More substance. If you know, you know.</p>
      </div>
    </section>
  </main>
</template>

<style scoped>
.hero__about {
  display: grid;
  place-items: center;
  text-align: center;
  gap: 0.5rem;
}

.hero__logo {
  height: clamp(56px, 8vw, 100px);
  width: auto;
}

.hero__title {
  font-size: clamp(1.6rem, 3.2vw, 2.4rem);
  letter-spacing: 0.01em;
  line-height: 1.15;
}

.hero__tagline {
  max-width: 70ch;
}

.list {
  margin: 0.25rem 0 0;
  padding-left: 1.1rem;
}

.list li + li { margin-top: 0.35rem; }

.pills {
  display: flex;
  gap: 0.5rem;
  margin: 0.25rem 0 0;
  padding: 0;
  list-style: none;
  flex-wrap: wrap;
}

.pills li {
  border: 1px solid rgba(255,255,255,0.12);
  background: rgba(255,255,255,0.04);
  border-radius: 999px;
  padding: 0.35rem 0.7rem;
  font-size: 0.95rem;
  white-space: nowrap;
}

.cta-row {
  margin-top: 0.75rem;
}
.statement {
  text-align: center;
  font-size: clamp(1.05rem, 1.2vw, 1.25rem);
  color: rgba(255,255,255,0.78);
}
</style>
