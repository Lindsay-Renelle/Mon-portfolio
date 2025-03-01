<template>
  <div id="app">
    <!-- Ajout du Header -->
    <Header />
    <header class="entete-contenu">
        <!-- Image de bienvenue -->
        <img src="@/assets/img-portfolio/Img-acceuil.jpg" alt="Image de bienvenue" class="image-gauche" />
      <!--Conteneur pour le texte-->
      <div class="texte-bienvenue">
        <h1>Bienvenue sur mon portfolio</h1>
      </div>
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
/* Style global pour html */
 body {
  background-color: #030660;
  height: 100%; /* Prendre toute la hauteur de la fenêtre */
  margin: 0;
  padding: 0;
}

/* Style global de l'application */
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  text-align: left;
  color: white;
  margin: 0;
  padding: 20px;
  /* Prendre toute la hauteur de la fenêtre */
  min-height: 100vh;
  height: 100%;
}

/* Conteneur de l'en-tête */
.entete-contenu {
  display: flex; /* Disposer les éléments en ligne */
  align-items: center; /* Alignement vertical */
  gap: 20px; /* Espacement entre l'image et le texte */
  width: 100%;
  justify-content: space-between;
}

/* Image de bienvenue */
.image-gauche {
  width: 400px;/*taille image*/
  height: auto;
  margin-top: 10px;/*Marge entre l'image et l'élement du dessus*/
  flex-shrink: 0; /* Empêcher l'image de rétrécir */
}

/* Texte de bienvenue */
.texte-bienvenue {
  flex-grow: 1; /* Prendre l'espace restant */
  font-size: 1.5em; /* Taille de la police */
  color: white; /* Couleur du texte */
  text-align: left;
  display: block;
  white-space: nowrap; /* Empêcher le retour à la ligne */
  overflow: hidden; /* Masquer le débordement */
  text-overflow: ellipsis; /* Ajouter des points de suspension si le texte déborde */
}

/* Contenu principal */
.contenu-principal {
 padding: 20px;
}
</style>