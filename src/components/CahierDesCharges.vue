<template>
  <div class="modal-item">
    <h4>Cahier des Charges</h4>
    <!-- Image cliquable -->
    <img src="../assets/img-portfolio/Cahier des charges.png" alt="Image Cahier des charges" class="cahier-image" @click="isOpen = true"/>
  
    <!--Mdale (visible seulement si isOpen est vrai)-->
    <div v-if="isOpen" class="modal">
      <div class="modal-content">
        <span class="close-button" @click="isOpen = false">&times;</span>
  
         <h4>Cahier des charges</h4>
        <p>
          Voici un exemple de cahier des charges que j'ai pu rédiger dans le cadre de ma formation. Il sert à cadrer un projet web
          en précisant les besoins, les objectifs, les fonctionnalités attendues, et les contraintes techniques.
        </p>
    
        <ul>
          <li>Objectifs du projet</li>
          <li>Public cible</li>
          <li>Fonctionnalités principales</li>
          <li>Technologies envisagées</li>
        </ul>
    
        <p>
          C’est un outil essentiel en début de projet pour bien communiquer entre les parties prenantes et organiser les étapes de
          réalisation.
        </p>
      </div>
    </div>
  </div>
</template>
  
  <script setup>
  import { ref } from 'vue'
  
  const isOpen = ref(false)
  </script>
  
  <style>
  .cahier-image {
    width: 200px;
    margin: 20px auto;
    cursor: pointer;
    border-radius: 10px;
    transition: transform 0.3s ease, box-shadow 0.3s ease;
  }
  
  .cahier-image:hover {
    transform: scale(1.05);
    box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2);
  }
  
  .modal {
    position: fixed;
    top: 0;
    left: 0;
    background: rgba(0, 0, 0, 0.7);
    width: 100%;
    height: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    z-index: 999;
  }
  
  .modal-content {
    background:#030660;
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
  