<template>
  <div class="marquee" aria-hidden="true">
    <div class="track">
      <span v-for="n in 2" :key="n" class="run">
        <span v-for="(item, i) in items" :key="i" class="item">
          {{ item }} <span class="sep">✦</span>
        </span>
      </span>
    </div>
  </div>
</template>

<script setup>
const items = [
  'NO SOFTNESS',
  'EXPOSED WIRING',
  'BUILT 2025',
  'HARD EDGES ONLY',
  'FILLER: NONE',
  'GOLEM-01',
]
</script>

<style scoped>
.marquee {
  overflow: hidden;
  border-bottom: 3px solid var(--ink);
  background: var(--accent);
  color: #111111;
  white-space: nowrap;
}
.track {
  display: inline-flex;
  animation: scroll 24s linear infinite;
}
.run {
  display: inline-flex;
  flex-shrink: 0;
}
.item {
  display: inline-flex;
  align-items: center;
  gap: 1.5rem;
  padding: 0.6rem 0;
  font-size: 0.8rem;
  font-weight: 700;
  letter-spacing: 0.25em;
}
.sep {
  font-size: 0.7rem;
}
@keyframes scroll {
  from {
    transform: translateX(0);
  }
  to {
    transform: translateX(-50%);
  }
}
</style>
