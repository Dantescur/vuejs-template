<script setup lang="ts">
import { ref } from 'vue'
import WebApp from '@twa-dev/sdk'

const count = ref(0)
</script>

<template>
  <header>
    <img alt="Vue logo" class="logo" src="./assets/logo.svg" width="125" height="125" />

    <div class="wrapper">
      <h1>Vite + Vue</h1>
      <div class="card">
        <button @click="count++">Count is: {{ count }}</button>
      </div>
    </div>
  </header>

  <main>
    <button @click="WebApp.showAlert(`Hello World! Current count is ${count}`)">Show Alert</button>
  </main>
</template>

<style scoped>
main {
  display: flex;
  justify-content: center;
  align-items: center;
}

button {
  min-height: 30px;
  background-color: #41b883;
  border: 2px solid white;
  border-radius: 4px;
  margin: 8px;
}

header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: center;
    flex-wrap: wrap;
  }
}
</style>
