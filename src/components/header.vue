<template>
  <header class="entete">
    <!--Barre de navigation-->
    <nav class="barre-navigation">
      <ul>
        <!--Liens vers les différentes sections de la page-->
        <li><a href="#je-suis">Qui suis-je ?</a></li>
        <li><a href="#competences">Mes compétences</a></li>
        <li><a href="#projets">Mes projets</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </nav>
  </header>
</template>

<style scoped>
  /* Conteneur de la barre de navigation */

  .barre-navigation {
    position: fixed;
  top: 0;
  right: 0;
  left: auto; /* Laisse la marge à droite */
  width: auto; /* Au lieu de 100%, pour éviter qu'elle disparaisse */
  background-color: #f4D7C8;
  height: 100px;
  z-index: 10;
  padding: 20px;
  border-radius: 10px;
  font-size: 20px;

}

 
/* Style de la liste de navigation */
.barre-navigation ul {
  /* Disposition des éléments en ligne */
  display: flex; 
  /* Supprime la marge par défaut */
  margin: 0; 
  /* Supprime le padding par défaut */
  padding: 0; 
  /* Enleve les puces de la liste */
  list-style-type: none; 
}

/* Style des liens de navigation */
.barre-navigation ul li a {
  /* Espace interne des liens */
  padding: 1.5rem; 
  /* Affichage des liens en bloc */
  display: block; 
  color: #030660; 
  /* Supprimer le soulignement */
  text-decoration: none; 
}

/* Styles pour les petites tailles d'écran */
@media screen and (max-width: 600px) {
  .conteneur-entete {
    /* Disposition en colonne*/
    flex-direction: column; 
  }

  .barre-navigation ul {
    /*Prends toute la largeur */
    width: 100%; 
    /* Disposition en colonne */
    flex-direction: column; 
  }

  .barre-navigation ul li {
    /* Aligner le texte au centre */
    text-align: center; 
  }
}
</style>

