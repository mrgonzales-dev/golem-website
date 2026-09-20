<template>
  <section id="specs" class="specs">
    <h2>/ SPECS</h2>
    <div class="grid">
      <div v-for="s in specs" :key="s.name" class="cell">
        <span class="name">{{ s.name }}</span>
        <span class="value">{{ s.value }}</span>
      </div>
    </div>
  </section>
</template>

<script setup>
const specs = [
  { name: 'CORE', value: 'CUSTOM' },
  { name: 'MODE', value: 'HARNESS' },
  { name: 'EDGE', value: 'HARD' },
  { name: 'FILLER', value: 'NONE' },
]
</script>

<style scoped>
.specs {
  padding: 3rem 2rem;
}
.grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  border: 3px solid var(--ink);
}
.cell {
  display: flex;
  flex-direction: column;
  gap: 0.5rem;
  padding: 1.5rem;
  border-right: 3px solid var(--ink);
  border-bottom: 3px solid var(--ink);
}
.name {
  font-size: 0.7rem;
  letter-spacing: 0.2em;
  opacity: 0.6;
}
.value {
  font-size: 1.25rem;
  text-transform: uppercase;
}
</style>
