<template>
  <section id="principles" class="principles">
    <h2>/ PRINCIPLES</h2>
    <ol class="list">
      <li v-for="(p, i) in principles" :key="p.title" class="row">
        <span class="num">{{ String(i + 1).padStart(2, '0') }}</span>
        <div class="body">
          <h3>{{ p.title }}</h3>
          <p>{{ p.text }}</p>
        </div>
        <span class="arrow">→</span>
      </li>
    </ol>
  </section>
</template>

<script setup>
const principles = [
  {
    title: 'EXPOSE EVERYTHING',
    text: 'No hidden seams, no decorative shells. If a wire carries load, you see the wire.',
  },
  {
    title: 'ZERO FILLER',
    text: 'Every panel, screw and pixel exists because it does work. Decoration is deleted on sight.',
  },
  {
    title: 'HARD BY DEFAULT',
    text: 'Impacts, weather, time. The harness is rated for all three before it is rated for looks.',
  },
  {
    title: 'REPAIR, NOT REPLACE',
    text: 'Every part is reachable with one tool. Nothing is glued shut. Nothing is a mystery.',
  },
]
</script>

<style scoped>
.principles {
  padding: 4rem 2rem;
  border-bottom: 3px solid var(--ink);
}
h2 {
  font-size: 1rem;
  letter-spacing: 0.2em;
  margin: 0 0 2rem;
}
.list {
  list-style: none;
  margin: 0;
  padding: 0;
  border-top: 3px solid var(--ink);
}
.row {
  display: flex;
  align-items: baseline;
  gap: 2rem;
  padding: 1.75rem 0.5rem;
  border-bottom: 3px solid var(--ink);
  transition: background 0.15s, color 0.15s;
}
.row:hover {
  background: var(--ink);
  color: var(--paper);
}
.num {
  font-size: 0.8rem;
  letter-spacing: 0.2em;
  opacity: 0.5;
  min-width: 2.5rem;
}
.body {
  flex: 1;
}
h3 {
  margin: 0 0 0.25rem;
  font-size: 1.1rem;
  letter-spacing: 0.15em;
}
p {
  margin: 0;
  font-size: 0.9rem;
  opacity: 0.7;
  max-width: 55ch;
  line-height: 1.5;
}
.arrow {
  opacity: 0;
  transition: opacity 0.15s;
}
.row:hover .arrow {
  opacity: 1;
}
</style>
