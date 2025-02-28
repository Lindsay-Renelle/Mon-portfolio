<template>
  <div id="app">
    <!-- Ajout du Header -->
    <Header />
    <header class="entete-contenu">
      <div class="section-gauche">
        <img src="@/assets/img-portfolio/Img-acceuil.jpg" alt="Image de bienvenue" class="image-gauche" />
      </div>
      <h1 class="texte-bienvenue">Bienvenue sur mon portfolio</h1>
    </header>
    <!-- Contenu principal où sont affichées les pages dynamiques -->
    <main class="contenu-principal">
      <router-view></router-view>
    </main>
    <!-- Ajout du Footer -->
    <Footer />
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    Header,
    Footer
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  text-align: left;
  color: white;
  background-color: #030660;
  margin: 0;
  padding: 20px;
  min-height: 100vh;
}

.entete-contenu {
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 100%;
  padding: 20px;
}
.section-gauche {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
}
.image-gauche {
  width: 150px;
  height: auto;
  margin-top: 10px;
}
.texte-bienvenue {
  flex: 1;
  text-align: right;
  font-size: 1.5rem;
}
.contenu-principal {
  padding: 20px;
}
</style>
