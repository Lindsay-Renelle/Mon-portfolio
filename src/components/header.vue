<template>
  <section class="entete-contenu">
    <h1>DUBOIS Céline</h1>
    <img src="@/assets/img-portfolio/Img-acceuil.jpg" alt="Image de bienvenue" class="image-gauche" width="350" height="350" />
    <div class="texte-bienvenue">
       <h2>Bienvenue sur mon portfolio</h2>
    </div>
  </section>
</template>


<style scoped>
.entete-contenu {
  color: #E6CBA8;
}
h1{
  font-size: 2.5em;
  margin-bottom: 10px;    /* Réduit l'espace sous le titre */
  padding: 0;
  margin-left: 5px;
}


img {
  margin-left: 15px;
  padding: 0;
  margin:5px 0 0 30px ;
  height: auto;
}

.texte-bienvenue {
  font-size: 2em;
  margin: 20px 0 0 60px ;
}
</style>
