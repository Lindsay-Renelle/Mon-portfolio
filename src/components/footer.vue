<template>
    <footer>
      <nav>
            <small class="social">
                <a href="https://www.facebook.com" target="_blank"><img src="../assets/img-portfolio/icon reseaux/facebook 1.png" alt="Facebook" class="social__icon"></a>
                <a href="https://www.linkedin.com/feed/" target="_blank"><img src="../assets/img-portfolio/icon reseaux/linkedin 1.png" alt="Linkedin" class="social__icon1"></a>
                <a href="https://github.com/Lindsay-Renelle" target="_blank"><img src="../assets/img-portfolio/icon reseaux/github 1.png" alt="GitHub" class="social__icon2"></a>
            </small>
            <p>Dernière mise à jour le <time datetime="2025/03/01">2 Avril 2025</time></p>
            <p>© Tous droits réservés.</p>
          </nav>
    </footer>
  </template>

  <style scoped>
footer {
    width: 100vw; /* Assure que le footer prend toute la largeur de la fenêtre */
    background-color: #030660; 
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 20px 0;
    position: relative;
    left: 0;
    min-height: 80px;/* Limite la hauteur du footer */
}
.social {
    display: flex;
    gap: 15px; /* Espacement entre les icônes */
    justify-content: center;
    align-items: center; /* Centre verticalement */
    width: 100%;
    padding: 10px;
}
footer nav {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    width: 100%;
    max-width: 1200px; /* Évite que le contenu soit trop étalé */
    text-align: center; /* Centrage du texte */
    background-color:#030660;
    padding: 10px;
    color: white;
}
.social a img {
    width: 40px; /* Taille raisonnable pour les icônes */
    height: 40px;
    transition: opacity 0.3s;
}
.social a img:hover {
    opacity: 0.6; /* Effet de survol */
}

.social__icon2 {
    background-color: white;
}
  </style>
  
  