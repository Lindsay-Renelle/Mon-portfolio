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
   
    <main>
      <div class="contenu-principal">
        <QuiSuisJe/>
        <Competence/>
        <!--Mes réalisations avec modals-->
        <section class="bloc-centrale">
          <h2> Mes réalisations</h2>
          <div class="modals-row">
            <div class="modal-item"><Cv/></div>
            <div class="modal-item"> <CahierDesCharges/></div>
            <div class="modal-item"><CoeurAPrendre/></div>
          </div>
        </section>

        <Contact/>
      </div>
      <router-view></router-view>
    </main>
    <!-- Ajout Footer -->
    <Footer />
  </div>
</template>

<script>
import Header from './components/Header.vue'
import QuiSuisJe from './components/QuiSuisJe.vue'
import Competence from './components/Competence.vue'
import Cv from './components/Cv.vue'
import CahierDesCharges from './components/CahierDesCharges.vue'
import CoeurAPrendre from './components/CoeurAPrendre.vue'
import Footer from './components/Footer.vue'
import Contact from './components/Contact.vue'

export default {
  name: 'App',
  components: {
    Header,
    QuiSuisJe,
    Competence,
    Cv,
    CahierDesCharges,
    CoeurAPrendre,
    Contact,
    Footer
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
  display: flex;
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
  gap: 10px;
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
main {
  width: 100%;
  display: flex;
  flex-direction: column; /* Met les blocs en colonne */
  align-items: center; /* Centre les blocs */
  gap: 40px; /* Espace entre chaque section */
}

/* Centrage et largeur des sections principales */
.contenu-principal > * {
  width: 250px;
  max-width: 1200px;
  margin: 0 auto;
  padding: 30px;
 
}

.bloc-centrale {
  display: flex;
  align-items: center;
  width: 100%;
}

/*modals*/
.modal-item {
  flex: 0 1 100px; /* Ne s'étire pas, garde une base de 300px */
  height: 150px;
  padding: 20px;
  box-sizing: border-box;
  border-radius: 12px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: flex-start;
  color: white;
  text-align: center;
  transition: transform 0.3s ease;
}

.modals-row {
  display: flex;
  gap: 20px;
  justify-content: center;
  align-items: flex-start;
  width: 100%;
  padding: 20px;
  box-sizing: border-box;
}

.modal-item:hover {
  transform: translateY(-5px);
  box-shadow: 0 10px 20px rgba(0,0,0,0.3);
}
</style>
