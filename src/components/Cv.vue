<template>
   <!-- Conteneur de la modale -->
  <div class="modal-item">

    <!-- Titre du projet -->
    <h4>Curriculum Vitae</h4>

    <!-- Image  cliquable-->
    <img
      src="../assets/img-portfolio/Img-visuel-cv.png"
      alt="Image CV"
       class="modal-image"
      @click="isModalOpen = true" 
      width="250"
      height="384"
    />

    <!-- Appel du composant modal, ouvert quand isModalOpen est true -->
    <Modal
      :isOpen="isModalOpen"    
      title="Curriculum Vitae"   
      date="Avril 2024"
      message="Voici mon CV et mes compétences en langage Web"
      technologie="HTML, CSS, JS"
      githubLink="https://github.com/Lindsay-Renelle/CV"
      @close="isModalOpen = false" />
  </div>
</template>

<script setup>
// On importe ref pour gérer une variable réactive
import { ref } from 'vue'
// Importation du  composant Modal
import Modal from './Modal.vue'

// Variable qui contrôle si la modale est ouverte
const isModalOpen = ref(false)
</script>

<style scoped>
/*Style sous-titre*/
h4{
  font-size: 1.5em;  /*Taille police*/
  margin-top: 5px;  /*Marge */
}

/*Style de l'image avant ouverture de la modale*/
.modal-image {
  max-width: 250px;                             /* Limite la largeur de l’image */
  height: auto;                                 /*Garde les proportions de l’image */
  cursor: pointer;                              /* Curseur en forme de main au survol */                    
  transition: transform 0.3s ease;              /*Transition douce pour les transformations et les ombres*/
  border-radius: 10px;                          /* Coins arrondis */
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);   /*ombre qui donne de la profondeur*/
}
/*Animation au survole*/
.modal-image:hover {
  transform: scale(1.05);                         /*Agrandit légèrement l’image au survol*/
  box-shadow: 0 12px 20px rgba(0, 0, 0, 0.3);   /*Ombre plus marquée au survol*/
  filter: brightness(1.05);                       /*Rend l’image légèrement plus lumineuse*/
}
</style>