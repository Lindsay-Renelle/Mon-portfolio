<template>
    <!-- Barre de navigation fixe -->
    <nav class="barre-navigation">
      <ul>
        <!--Lien de navigation-->
        <li><a href="#je-suis">Qui suis-je ?</a></li>
        <li><a href="#competences">Mes compétences</a></li>
        <li><a href="#realisations">Mes réalisations</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </nav>
  </template>

 
<style scoped>
/* Style de la barre de navigation */
.barre-navigation {
  position: fixed;           /* Fixe la barre en haut à droite de l'écran */
  top: 20px;
  right: 20px;
  background-color: #f4D7C8; /* Couleur de fond */
  padding: 10px 15px;        /* Espace intérieur */
  border-radius: 8px;        /* Coins arrondis */
  z-index: 1000;             /* S'assure que la barre passe au-dessus du reste */
}

/* Style de la liste des liens */
.barre-navigation ul {
  display: flex;             /* Affiche les éléments en ligne */
  flex-direction: row;       /* Orientation horizontale */
  margin: 0;
  padding: 0;
  list-style-type: none;     /* Supprime les puces de liste */
  gap: 15px;                 /* Espace entre les liens */
}

/* Style général des liens */
.barre-navigation ul li a {
  display: block;
  color: #030660;           /* Couleur du texte */
  text-decoration: none;      /* Supprime le soulignement par défaut */
  padding: 8px 12px;          /* Espace autour du texte */
  border-radius: 4px;         /* Coins arrondis */
  font-size: 15px;
  transition: all 0.3s ease;  /* Animation douce */
}

/* Effet de survol (hover) */
.barre-navigation ul li a:hover {
  background-color: #f2aa4bbe;
  text-decoration: underline;
}

/* Effet au clic (active) */
.barre-navigation ul li a:active {
  background-color: #eecfc0be;
  text-decoration: underline;
}
</style>

  