<template>
  <div class="modal-item">
    <h4>Cahier des charges</h4>

    <!-- Image cliquable -->
    <img
      src="../assets/img-portfolio/Cahier des charges.png"
      alt="Image Cahier des charges"
      class="cahier-image"
      @click="isModalOpen = true" 
    />

    <!-- Appel de la modal -->
    <Modal
      :isOpen="isModalOpen"       
      title="Cahier des charges"   
      message="Exemple de cahier des charges que j'ai rédigé dans le cadre de ma formation. Il sert à cadrer un projet web." 
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
.cahier-image {
  width: 200px;
  cursor: pointer;
}
</style>
