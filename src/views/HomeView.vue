<template>
    <!-- Supprime le composant TheWelcome -->
</template>

<script setup>
import { ref, onMounted } from "vue";

const utilisateur = ref("");

// Sauvegarde automatique dans localStorage
function sauvegarder() {
  localStorage.setItem("nomUtilisateur", utilisateur.value);
}

// Chargement automatique au démarrage
onMounted(() => {
  utilisateur.value = localStorage.getItem("nomUtilisateur") || "";
});
</script>