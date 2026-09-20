<template>
  <header class="header">
    <span class="logo">GOLEM_</span>
    <nav>
      <a href="#manifesto">MANIFESTO</a>
      <a href="#specs">SPECS</a>
      <a href="#download">DOWNLOAD</a>
    </nav>
  </header>
</template>

<style scoped>
.header {
  position: sticky;
  top: 0;
  z-index: 10;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1rem 2rem;
  background: var(--paper);
  border-bottom: 3px solid var(--ink);
}
.logo {
  font-size: 1.5rem;
  letter-spacing: 0.2em;
}
nav {
  display: flex;
  gap: 1.5rem;
}
a {
  color: var(--ink);
  text-decoration: none;
  font-size: 0.8rem;
  letter-spacing: 0.1em;
}
a:hover {
  background: var(--accent);
  border-color: var(--accent);
  color: #111111;
}
</style>
