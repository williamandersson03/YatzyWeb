<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <header>
    <div class="logodiv">
      <img alt="YatzyWeb logo" class="logo" src="@/assets/logo.svg" width="80" height="80" />
      <h1>YatzyWeb</h1>
    </div>
    <div class="wrapper">
      <nav>
        <RouterLink to="/">Hem</RouterLink>
        <RouterLink to="/about">Om projektet</RouterLink>
      </nav>
    </div>
  </header>
  <div class="routerviewbody">
    <RouterView />
  </div>
</template>

<style scoped>

header {
  line-height: 1.5;
  max-height: 100vh;
  display: flex;
  justify-content: center;
  flex-direction: column;
  align-items: center;
}

@media (max-width: 1023px) {
  .routerviewbody {
    display: flex;
    justify-content: center;
    flex-direction: column;
  }
}
@media (min-width: 1024px) {
  .routerviewbody {
    display: flex;
    justify-content: center;
  }
}

.logo {
  display: block;
  margin: 0 auto;
}

.logodiv {
  display: flex;
  flex-direction: column;
  align-items: center;
}
.logodiv h1 {
  color: white;
}

nav {
  width: 100%;
  font-size: 18px;
  text-align: center;
  margin-top: 1.2rem;
}

nav a.router-link-exact-active {
  color: var(--color-text);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {
  display: inline-block;
  padding: 0 1rem;
  border-left: 1px solid var(--color-border);
}

nav a:first-of-type {
  border: 0;
}
</style>
