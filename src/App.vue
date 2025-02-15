<template>
  <div id="app">
    <Header /> <!-- Utiliser le composant Header ici -->
    <img alt="Vue logo" class="logo" src="@/assets/logo.svg" width="125" height="125" />
    <div class="wrapper">
      <HelloWorld msg="You did it!" />
      <nav>
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/about">About</RouterLink>
      </nav>
    </div>
    <router-view />
    <Footer /> <!-- Utiliser le composant Footer ici -->
  </div>
</template>

<script setup>
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'
import Header from './components/Header.vue' // Importation du composant Header
import Footer from './components/Footer.vue' // Importation du composant Footer
</script>

<style scoped>
/* Ajoute tes styles personnalisés ici */
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  line-height: 1.5;
  min-height: 100vh;
}
.wrapper {
  text-align: center;
  margin-top: 60px;
}
nav {
  display: flex;
  justify-content: center;
  gap: 15px;
  margin-top: 20px;
}
nav a {
  color: #42b983;
  text-decoration: none;
}
nav a:hover {
  text-decoration: underline;
}
</style>
