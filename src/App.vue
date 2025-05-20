<template>
  <div id="tool">
    <!--Ceci est la page 404 (NotFound)-->
    <router-view v-if="isNotFoundPage" />
    <!--Sinon : page normal-->
    <template v-else>
      <!--Ajout du Header-->
      <Header/>
      <Navigation/>
        <!-- Contenu principal où sont affichées les pages dynamiques -->
      <main>
        <div class="contenu-principal">
          <QuiSuisJe />
          <Competence />
          <section class="bloc-modal">
            <h3 id="realisations">Mes réalisations</h3>
            <div class="modal">
              <Cv />
              <CahierDesCharges />
              <CoeurAPrendre />
            </div>
          </section>
          <Contact />
        </div>
        <router-view/>
      </main>
      <!-- Ajout Footer --> 
      <Footer />
    </template>
  </div>
</template>

<script setup>
import { computed } from 'vue'
import { useRoute } from 'vue-router'

import Header from './components/Header.vue'
import Navigation from './components/Navigation.vue'
import QuiSuisJe from './components/QuiSuisJe.vue'
import Competence from './components/Competence.vue'
import Cv from './components/Cv.vue'
import CahierDesCharges from './components/CahierDesCharges.vue'
import CoeurAPrendre from './components/CoeurAPrendre.vue'
import Contact from './components/Contact.vue'
import Footer from './components/Footer.vue'

// ➕ Ici, on récupère la route actuelle
const route = useRoute()

// ➕ Vérifie si le nom de la route est "NotFound"
const isNotFoundPage = computed(() => route.name === 'NotFound')
</script>

<style scoped>
h3 {
  color: #E6A8A8;
  font-size: 2em;         /*Augmente la taille du titre*/
  font-weight: bold;
  text-align: center;     /*Centre le titre*/ 
  margin-top: 30px;       /*Espacement entre l’image et le titre*/
}

main {
  display: flex;
  flex-direction: row-reverse;
  justify-content: center;
  align-items: center;
}

.modal {
  display: flex;
  justify-content: center;  /*Centre horizontalement*/
  align-items: center;      /*Centre verticalement (utile si hauteur fixe)*/
  flex-wrap: wrap;          /*Permet de passer à la ligne sur petit écran*/
  gap: 40px;                /*Espace entre les images */
  margin-top: 20px;
}

.modal-item {
  text-align: center;
}
</style>