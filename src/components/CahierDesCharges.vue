<template>
  <div class="modal-item">
    <h4>Cahier des charges</h4>

    <!-- Image cliquable -->
    <img
      src="../assets/img-portfolio/Cahier des charges.png"
      alt="Image Cahier des charges"
      class="modal-image"
      @click="isModalOpen = true" 
    />

    <!-- Appel de la modal -->
    <Modal
      :isOpen="isModalOpen"       
      title="Cahier des charges"
      date="Mai 2024" 
      message="Exemple de cahier des charges que j'ai rédigé dans le cadre de ma formation. Il sert à cadrer un projet web." 
      technologie="PDF"
      pdfLink="pdf/cahier-des-charges.pdf"
      @close="isModalOpen = false" 
    />
  </div>
</template>

<script setup>
// On importe ref pour gérer une variable réactive
import { ref } from 'vue'
// On importe le composant Modal
import Modal from './Modal.vue'

// Variable qui contrôle si la modale est ouverte
const isModalOpen = ref(false)
</script>

<style scoped>
/*Style sous-titre*/
h4 {
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


