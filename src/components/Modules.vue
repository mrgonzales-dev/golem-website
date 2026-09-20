<template>
  <section id="modules" class="modules">
    <h2>/ MODULES</h2>
    <div class="grid">
      <article v-for="m in modules" :key="m.code" class="card">
        <header class="card-head">
          <span class="code">{{ m.code }}</span>
          <span class="status" :class="{ live: m.live }">
            {{ m.live ? '● LIVE' : '○ DEV' }}
          </span>
        </header>
        <h3>{{ m.name }}</h3>
        <p>{{ m.desc }}</p>
        <footer class="card-foot">
          <span v-for="tag in m.tags" :key="tag" class="tag">{{ tag }}</span>
        </footer>
      </article>
    </div>
  </section>
</template>

<script setup>
const modules = [
  {
    code: 'M-01',
    name: 'CORE FRAME',
    desc: 'Load-bearing exo-skeleton. Titanium rails, zero flex under rated torque.',
    tags: ['TI', 'RATED 400KG'],
    live: true,
  },
  {
    code: 'M-02',
    name: 'NERVE BUS',
    desc: 'Single exposed wiring channel. Every line labeled, every connector serviceable.',
    tags: ['CAN', 'IP67'],
    live: true,
  },
  {
    code: 'M-03',
    name: 'JOINT SET',
    desc: 'Six degrees of freedom per limb. Hard stops, no dampening, no surprises.',
    tags: ['6DOF', 'STEEL'],
    live: true,
  },
  {
    code: 'M-04',
    name: 'SKIN PLATE',
    desc: 'Optional. Raw brushed panels for environments that demand coverage.',
    tags: ['OPTIONAL'],
    live: false,
  },
]
</script>

<style scoped>
.modules {
  padding: 4rem 2rem;
  border-bottom: 3px solid var(--ink);
}
h2 {
  font-size: 1rem;
  letter-spacing: 0.2em;
  margin: 0 0 2rem;
}
.grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
  gap: 1.5rem;
}
.card {
  border: 3px solid var(--ink);
  padding: 1.5rem;
  display: flex;
  flex-direction: column;
  gap: 0.75rem;
  transition: background 0.15s, color 0.15s;
}
.card:hover {
  background: var(--ink);
  color: var(--paper);
}
.card-head {
  display: flex;
  justify-content: space-between;
  font-size: 0.7rem;
  letter-spacing: 0.2em;
  opacity: 0.7;
}
.status.live {
  color: var(--accent);
}
h3 {
  margin: 0;
  font-size: 1.25rem;
  letter-spacing: 0.1em;
}
p {
  margin: 0;
  font-size: 0.85rem;
  line-height: 1.5;
  opacity: 0.7;
  flex: 1;
}
.card-foot {
  display: flex;
  flex-wrap: wrap;
  gap: 0.5rem;
}
.tag {
  font-size: 0.65rem;
  letter-spacing: 0.15em;
  border: 2px solid currentColor;
  padding: 0.2rem 0.5rem;
}
</style>
