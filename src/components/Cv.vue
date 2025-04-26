<template>
  <div class="modal-item">
    <h4>Curriculum Vitae</h4>

    <!-- Image cliquable -->
    <img
      src="../assets/img-portfolio/Img-visuel-cv.png"
      alt="Image CV"
      class="cv-image"
      @click="isModalOpen = true" 
    />

    <!-- Appel de la modal -->
    <Modal
      :isOpen="isModalOpen"       
      title="Curriculum Vitae"   
      message="Voici mon CV avec mes compétences en HTML, CSS, JavaScript." 
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
.cv-image {
  width: 200px;
  cursor: pointer;
}
</style>
