<template>
   <!-- Conteneur principal -->
   <div class="not-found">
      <!-- Image d'erreur personnalisée -->
      <img src="../assets/img-portfolio/Image 404.png" alt="Erreur 404" />
  
      <!-- Titre principal de la page 404 -->
      <h1>Oups ! Cette page n'existe pas.</h1>
  
      <!-- Message complémentaire pour l'utilisateur -->
      <p>Il semble que vous soyez perdu(e)...</p>
  
      <!-- Lien pour retourner à la page d'accueil -->
      <router-link to="/">Retour à l'accueil</router-link>
    </div>
  </template>

<script setup>
</script>

<style scoped>
/* Style composant */
.not-found {
  text-align: center;      /* Centre  horizontalement */
  padding: 40px;           /*Espace autour du contenu */
  color: white;          
}

/* Style de l'image 404 */
.not-found img {
  width: 300px;            /* Largeur fixe */
  max-width: 80%;          /* Responsive : au max 80% de la largeur du conteneur */
  margin-bottom: 20px;     
}

/* Style du lien de retour à l'accueil */
.not-found a {
  display: inline-block;   /* Rend le lien stylable comme un bloc */
  margin-top: 20px;        /* Espace au-dessus du lien */
  padding: 10px 20px;      
  background-color: #ffc0cb; 
  color: #000;             
  text-decoration: none;  
  border-radius: 5px;     
}
</style>