<template>
  <div class="modal-item">
    <h4>Curriculum Vitae</h4>

    <!--Image cliquable-->
    <img src="../assets/img-portfolio/Img-visuel-cv.png" alt="Image CV" class="cv-image" @click = "isOpen = true"/>

    <!--Mdale (visible seulement si isOpen est vrai)-->
    <div v-if ="isOpen" class ="modal">
      <div class="modal-content">
        <span class="close-button" @click="isOpen = false"> &times;</span>

          <h4>Notions en développement</h4>
          <p>
            Je suis actuellement en formation pour devenir développeur front-end. <br>
            J’apprends les bases du HTML, CSS et JavaScript, et je construis petit à petit mon portfolio.
          </p>

          <ul class="list">
            <li>Créer une page web en HTML</li>
            <li>Styliser avec CSS (couleurs, layout, flexbox)</li>
            <li>Faire des interactions simples avec JavaScript (ex : bouton, modale)</li>
          </ul>
          <p>
             Mon but est de continuer à progresser, apprendre Vue.js, et créer des projets concrets pour gagner en expérience.
          </p>
      </div>
    </div>
</div>
</template>

<script setup>
import { ref } from 'vue'

// isOpen contrôle l’affichage de la modale
const isOpen = ref(false)
</script>


<style>
.cv-image {
  width: 200px;
  cursor: pointer;
  border-radius: 10px;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.cv-image:hover {
  transform: scale(1.05);
  box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2);
}

.modal {
  position: fixed;
  top: 0;
  left: 0;
  background-color:#060f91 ;
  width: 100%;
  height: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 999;
}

.modal-content {
  background: #030660;
  padding: 30px;
  width: 90%;
  max-width: 600px;
  border-radius: 12px;
  box-shadow: 0 10px 25px rgba(0, 0, 0, 0.3);
  text-align: left;
  color: bisque;
}

.close-button {
  font-size: 28px;
  float: right;
  cursor: pointer;
  color: #888;
}

.close-button:hover {
  color: #000;
}
</style>