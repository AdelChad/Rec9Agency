<template>
  <header>
    <div class="wrapper">
      <Titre/>
    </div>
    <Navbar class="navbar menu-item_sub"/>
  </header>

  <main>
    <Accueil />
  </main>
</template>

<script setup>
import Titre from './components/Titre.vue'
import Navbar from './components/Navbar.vue'
import Accueil from './components/Accueil.vue'
</script>

<style scoped>
header {
  line-height: 1.5;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    padding-right: calc(var(--section-gap) / 2);
  }

  header .wrapper {
    overflow: hidden;
    background-color: #333;
    position: fixed;
    left: 0;
    top: 0;
    width: 100%; 
  }
}

.navbar {
  font-size: 2vh;
  top: 14%;
  left: 50%;
  transform: translate(-50%, -50%);
  position: fixed;
}
</style>
