<template>
  <section id="download" class="cta">
    <div class="inner">
      <p class="kicker">// GET THE HARNESS</p>
      <h2>BUILD<br />YOUR GOLEM.</h2>
      <p class="sub">Specs, CAD files and the full parts list. Free. No email wall.</p>
      <div class="actions">
        <a href="#" class="btn primary">DOWNLOAD KIT ↓</a>
        <a href="#specs" class="btn">READ SPECS</a>
      </div>
    </div>
  </section>
</template>

<style scoped>
.cta {
  padding: 6rem 2rem;
  border-bottom: 3px solid var(--ink);
  text-align: center;
}
.kicker {
  font-size: 0.75rem;
  letter-spacing: 0.3em;
  color: var(--accent);
  margin: 0 0 1rem;
}
h2 {
  font-size: clamp(2.5rem, 8vw, 6rem);
  letter-spacing: -0.02em;
  margin: 0;
  text-transform: uppercase;
}
.sub {
  opacity: 0.7;
  font-size: 1rem;
  margin: 1.5rem auto 2.5rem;
  max-width: 45ch;
}
.actions {
  display: flex;
  gap: 1rem;
  justify-content: center;
  flex-wrap: wrap;
}
.btn {
  display: inline-block;
  padding: 1rem 2.5rem;
  border: 3px solid var(--ink);
  color: var(--ink);
  text-decoration: none;
  font-size: 0.85rem;
  font-weight: 700;
  letter-spacing: 0.2em;
  transition: background 0.15s, color 0.15s, border-color 0.15s;
}
.btn:hover {
  background: var(--paper);
  color: #111111;
  border-color: var(--paper);
}
.btn.primary {
  background: var(--accent);
  color: #111111;
  border-color: var(--accent);
}
.btn.primary:hover {
  background: var(--paper);
  border-color: var(--paper);
}
</style>
