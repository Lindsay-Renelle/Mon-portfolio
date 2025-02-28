<template>
  <header class="conteneur-entete">
    <!--Titre-->
    <h1 class="titre">DUBOIS Céline</h1>
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
/* Conteneur de l'en-tête */
.conteneur-entete {
  /*Dispositon du contenu en ligne*/
  display: flex;
  /*Espacement égal entre les éléments*/
  justify-content: space-between;
  /*Espacement égal entre les éléments*/
  align-items: center;
  /* Fixer l'en-tête en haut de la page */
  position: fixed; 
  /*Largeur de l'entête*/
  width: 100%;
  /*Espace interne autour d du conteneur'*/
  padding: 20px;
}

/* Style du titre */
.titre {
  /*Taille de police*/
  font-size: 3em;
  /*Supprimer la marge par défaut*/
  margin: 0;
}

/* Conteneur de la barre de navigation */
.barre-navigation {
 /*Couleur de fond de la barre de navigation*/
 background-color:#f4D7C8 ;
 /*Espacement interne*/
 padding: 20px;
 /*Bordure arrondie*/
 border-radius: 10px;
 /* Permet à la barre de navigation de prendre plus de place */
 flex-grow: 0.1;
 /*Marge*/
 margin-left: 800px;
 margin-right: 40px;
 /*Police*/
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

  .barre-navigation ul li a {
    /* Espacement des liens pour les petits écrans */
    padding: 5rem 1rem; 
  }
}
</style>
