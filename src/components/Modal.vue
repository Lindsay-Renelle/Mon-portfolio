<template>
      <!--Modale affichée seulement si "isOpen" est true-->
      <div
        v-if="isOpen" class="modal" @click="handleOutsideClick">                                                  
        <div class="modal-box"  ref="modalBox">
          <h4>{{ title }}</h4>                                            <!-- Affiche le titre passé en prop -->
          <p class="date">Date : {{ date }}</p>                           <!--Date du projet-->
          <p>{{ message }}</p>                                            <!-- Affiche le message passé en prop -->
          <p class="technologies">Technologies : {{ technologie }}</p>    <!--Technologies utilisées-->

          <!-- Affiche le lien GitHub uniquement s’il est fourni -->
          <p v-if="githubLink" class="lien"> 
            <a :href= "githubLink" target="_blank">Voir le projet sur GitHub</a>
          </p>

          <!-- Affiche le lien vers le PDF uniquement s’il est fourni -->
          <p v-if="pdfLink" class="lien">
            <a :href="pdfLink" target="_blank">Voir le PDF</a>
          </p>
          <div class="modal-button-container">
            <button @click="$emit('close')">Fermer</button>           <!-- Émet l'événement 'close' pour prévenir le parent -->    
          </div>           
        </div>
      </div>
</template>

<script setup>
//Importation "ref" depuis Vue pour créer une référence vers un élément HTML
import { ref } from 'vue'

// Récupèration des props envoyées par le parent
defineProps({
  isOpen: Boolean,
  title: String,
  date: String,
  message: String,
  technologie: String,
  githubLink: String,
  pdfLink: String,
})

// Déclaration des événements que ce composant peut émettre (ici, juste 'close')
const emit = defineEmits(['close'])

//Création d'une référence vers la boîte modale pour y accéder dans le code
const modalBox = ref(null)

// Fonction qui sera appelée quand on clique n’importe où sur le fond.
function handleOutsideClick(event) {

  // Si on clic en dehors alors on ferme la modale.
  if (modalBox.value && !modalBox.value.contains(event.target)) {
    emit('close') // Déclanchement de l’événement 'close' demande au parent de fermer la modale
  }
}
</script>

<style scoped>
/* Fond semi-transparent */
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

/* Contenu de la modale */
.modal-box {
  background: #f4D7C8;
  color: black;
  padding: 25px;
  max-width: 500px;
  border-radius: 10px;
  box-shadow: 0 8px 20px rgba(0, 0, 0, 0.3);
  font-family: Arial, sans-serif;
}

.modal-box h4 {
  font-size: 1.6em;
  margin-bottom: 15px;
}

a {
  color: #1abc9c;
  font-weight: bold;
  text-decoration: none;
}

 a:hover {
  text-decoration: underline;
}

/*Bouton "Fermer"*/
.modal-button-container {
  display: flex;
  justify-content: center; /* Centre horizontalement */
  margin-top: 20px;        /* Un peu d'espace au-dessus */
}
</style>
