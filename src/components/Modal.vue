<template>
  <div v-if="isOpen" class="modal">
    <div class="modal-box">
      <h4>{{ title }}</h4> <!-- Affiche le titre passé en prop -->
      <p>{{ message }}</p> <!-- Affiche le message passé en prop -->
      <button @click="$emit('close')">Fermer</button> <!-- Émet l'événement 'close' pour prévenir le parent -->
    </div>
  </div>
</template>

<script setup>
// On récupère les props envoyées par le parent
defineProps({
  isOpen: Boolean,
  title: String,
  message: String
})
</script>

<style scoped>
.modal {
  position: fixed;
  top: 0;
  left: 0;
  width: 100vw;
  height: 100vh;
  background-color: rgba(0, 0, 0, 0.5);
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 1000;
}

.modal-box {
  background: white;
  color: black;
  padding: 20px;
  max-width: 500px;
  border: 1px solid #ccc;
}
</style>
