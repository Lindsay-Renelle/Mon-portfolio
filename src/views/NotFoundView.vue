<template>
  <!-- Composant en-tête global -->
  <Header />

  <!-- Conteneur principal -->
  <div class="not-found" role="main" aria-label="Page non trouvé">
    <!-- Image d'erreur personnalisée -->
    <img src="../assets/img-portfolio/Image 404.png" alt="Erreur 404 - Page non trouvée" />
  
    <!-- Titre principal de la page 404 -->
    <h1>Oups ! Cette page n'existe pas.</h1>
  
    <!-- Message complémentaire pour l'utilisateur -->
    <p>Il semble que vous soyez perdu(e)...</p>
  
    <!-- Lien pour retourner à la page d'accueil -->
    <router-link to="/"aria-label="Retourner à la page d'accueil">Retour à l'accueil</router-link>
  </div>

  <!-- Composant pied de page global -->
  <Footer />
</template>

<script setup>
// Importe les composants Header et Footer
import Header from '@/components/Header.vue'
import Footer from '@/components/Footer.vue'
</script>

<style scoped>
/* Style composant */
.not-found {
  text-align: center;          
  padding: 40px;               
  color: white;
  background-color: #030660;    
  display: flex; 
  flex-direction: column;      
  justify-content: center;     
  align-items: center;            
}

/* Style de l'image 404 */
.not-found img {
  width: 300px;            /* Largeur fixe */
  max-width: 80%;          /* Responsive : au max 80% de la largeur du conteneur */
  margin-bottom: 20px;     /* Marge sous l'image*/
}

/* Style du lien de retour à l'accueil */
.not-found a {
  display: inline-block;   
  margin-top: 20px;        /* Espace au-dessus du lien */
  padding: 10px 20px;      
  background-color: #f4D7C8; 
  color: #000;             
  text-decoration: none;  
  border-radius: 5px;    
  transition: background 0.3s; 
}
/* Effet au survol */
.not-found a:hover {
  background-color: #f2aa4bbe;
}
</style>