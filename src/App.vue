<template>
  <div id="app">
    <!-- Ajout du Header -->
    <Header />
    <section class="entete-contenu">
      <!--Titre principal-->
      <h1>DUBOIS Céline</h1>

      <!-- Image de bienvenue -->
      <img src="@/assets/img-portfolio/Img-acceuil.jpg" alt="Image de bienvenue" class="image-gauche" />

      <!--Conteneur pour le texte-->
      <div class="texte-bienvenue">
        <h2>Bienvenue sur mon portfolio</h2>
      </div>
    </section>

    <!-- Contenu principal où sont affichées les pages dynamiques -->
    <main class="contenu-principal">
      <div class="about-container">
        <AboutMe />
      </div>
      <router-view></router-view>
    </main>
    <!-- Ajout Footer -->
    <Footer />
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Footer from './components/Footer.vue'
import AboutMe from './components/AboutMe.vue'

export default {
  name: 'App',
  components: {
    Header,
    Footer,
    AboutMe,
  },
}
</script>

<style>
/* Style du titre */
h1 {
  text-align: center;
  font-size: 3em;
}

/* Style global pour html */
body {
  background-color: #030660;
  margin: 0;
  padding: 0;
  height: 100%; /* Prends toute la hauteur de la fenêtre */
}

/* Style global de l'application */
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  color: white;
  margin: 0;
  padding: 20px;
  min-height: 100vh;
  display: block;
  flex-direction: column;
  align-items: center; /* Centre tout le contenu */
  text-align: center; /* Centre le texte */
}

/* Conteneur de l'en-tête */
.entete-contenu {
  display: flex;
  flex-direction: column;
  align-items: flex-start; /* Aligne tous sur la gauche */
  width: 100%;
  gap: 10px;  /* Espacement entre l'image et le texte */
}

/* Image de bienvenue */
.image-gauche {
  width: 400px;
  height: auto;
  margin-left: 8%;
}

/* Texte de bienvenue */
.texte-bienvenue {
  font-size: 1.5em;
  color: white;
  text-align: left;
  margin-left: 16%;
}

/* Contenu principal */
.contenu-principal {
  width: 100vw; /* Prend toute la largeur */
  height: auto; /* Ajuste la hauteur */
  min-height: 300px; /* Assure qu’il est visible */
  display: flex;
  flex-direction: row;
  align-items: flex-start;
  justify-content: space-around;
}

.about-container {
  width:50%;
  max-width: none;
  padding: 0 20px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}
</style>
