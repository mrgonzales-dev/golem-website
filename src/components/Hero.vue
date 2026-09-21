<template>
  <section class="hero">
    <p class="kicker">// UNIT 001 — FIELD READY</p>
    <h1>GO<em>LEM</em></h1>
    <p class="tag">CUSTOM HARNESS. NO SOFTNESS.</p>
    <div class="meta">
      <span>EST. SEP 2026</span>
      <span>WIRES: EXPOSED</span>
      <span>WEIGHT: 84KG</span>
    </div>
  </section>
</template>

<style scoped>
.hero {
  position: relative;
  padding: 6rem 2rem 4rem;
  border-bottom: 3px solid var(--ink);
  background-image: var(--scratches), radial-gradient(ellipse at 20% 10%, rgba(200, 255, 0, 0.08), transparent 55%),
    radial-gradient(ellipse at 85% 90%, rgba(244, 242, 236, 0.06), transparent 50%);
  overflow: hidden;
}
.hero::before {
  content: '';
  position: absolute;
  inset: 0;
  background: var(--noise);
  opacity: 0.25;
  pointer-events: none;
}
.hero::after {
  content: '';
  position: absolute;
  left: -10%;
  right: -10%;
  bottom: -2px;
  height: 6px;
  background: var(--accent);
  transform: rotate(-0.6deg);
  opacity: 0.5;
}
.hero > * {
  position: relative;
}
.kicker {
  font-size: 0.75rem;
  letter-spacing: 0.3em;
  color: var(--accent);
  margin: 0 0 1rem;
}
h1 {
  font-size: clamp(4rem, 14vw, 12rem);
  letter-spacing: -0.03em;
  line-height: 0.9;
  margin: 0;
}
h1 em {
  font-style: normal;
  color: var(--accent);
}
.tag {
  font-size: 1rem;
  letter-spacing: 0.3em;
  margin-top: 1rem;
}
.meta {
  display: flex;
  gap: 2rem;
  flex-wrap: wrap;
  margin-top: 2.5rem;
  font-size: 0.7rem;
  letter-spacing: 0.2em;
  opacity: 0.6;
}
</style>
