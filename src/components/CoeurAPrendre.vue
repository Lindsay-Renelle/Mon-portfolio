<template>
  <div class="modal-item">
    <h4>Coeur à prendre</h4>

    <!-- Image cliquable -->
    <img
      src="../assets/img-portfolio/Img-visuel-site.png"
      alt="Image Coeur à prendre"
      class="site-image"
      @click="isModalOpen = true" 
    />

    <!-- Appel de la modal -->
    <Modal
      :isOpen="isModalOpen"       
      title="Coeur à prendre"   
      message="Ce site a été conçu pour mettre en pratique et améliorer mes compétences en développement web." 
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
.site-image {
  width: 200px;
  cursor: pointer;
}
</style>
