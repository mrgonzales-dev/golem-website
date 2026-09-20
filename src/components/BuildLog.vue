<template>
  <section id="log" class="log">
    <h2>/ BUILD LOG</h2>
    <div class="entries">
      <div v-for="e in entries" :key="e.date + e.title" class="entry">
        <span class="date">{{ e.date }}</span>
        <span class="title">{{ e.title }}</span>
        <span class="hash">{{ e.hash }}</span>
      </div>
    </div>
  </section>
</template>

<script setup>
const entries = [
  { date: '2025-11-02', title: 'Nerve bus re-routed, single channel', hash: 'a3f9c1e' },
  { date: '2025-10-18', title: 'Joint set v4 — hard stops only', hash: '7b2d40f' },
  { date: '2025-09-30', title: 'Removed remaining filler panels', hash: 'c81aa62' },
  { date: '2025-09-07', title: 'Load test: 400kg, 6h, zero deflection', hash: 'e05f113' },
]
</script>

<style scoped>
.log {
  padding: 4rem 2rem;
  border-bottom: 3px solid var(--ink);
}
h2 {
  font-size: 1rem;
  letter-spacing: 0.2em;
  margin: 0 0 2rem;
}
.entries {
  border-top: 3px solid var(--ink);
}
.entry {
  display: grid;
  grid-template-columns: 9rem 1fr 6rem;
  gap: 1rem;
  padding: 1rem 0.5rem;
  border-bottom: 3px solid var(--ink);
  font-size: 0.85rem;
  transition: background 0.15s, color 0.15s;
}
.entry:hover {
  background: var(--ink);
  color: var(--paper);
}
.date {
  opacity: 0.5;
  letter-spacing: 0.1em;
}
.hash {
  text-align: right;
  color: var(--accent);
  letter-spacing: 0.1em;
}
@media (max-width: 600px) {
  .entry {
    grid-template-columns: 1fr 5rem;
  }
  .date {
    grid-column: 1 / -1;
  }
}
</style>
