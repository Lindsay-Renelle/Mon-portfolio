<template>
        <section id="contact"  class="contact">
            <h3>Contactez-moi</h3>
            <!-- Formulaire.--> 
            <form>
                <input type="text" placeholder="Nom" >
                <input type="email" placeholder="Email">
                <textarea placeholder="Message"></textarea>
                <!--Bouton envoyer-->
                <input type="submit" value="Envoyer">
            </form>
        </section>
</template>


<style scoped>
/* style de h2 */
h3 {
    color: #C6A8E6;
    font-family: 'Lobster';         /* Police */
    font-size: 2em;                 /* Augmente la taille du titre */
    font-weight: bold;              /* Met le texte en gras*/
    text-align: center;             /* Centre le titre */ 
    margin-top: 15px;               /* Espacement entre l’image et le titre */
}

.contact {
  margin : auto;
  padding-top: 30px;
}

/* Section formulaire */
.contact form {
    display: flex;              /* Flexbox pour aligner les éléments */
    flex-direction: column;     /* Eléments en colonne */
    align-items: center;        /* Centre les éléments horizontalement */
    width: 50%;                 /* Le formulaire prend 50% de la largeur disponible */
    max-width: 300px;           /* Évite qu'il devienne trop large sur les grands écrans */
    margin: 0 auto;             /* Centre le formulaire */
}

/* Champs texte et message */
.contact input, 
.contact textarea {
    width: 100%;                /* Prend toute la largeur disponible */
    padding: 15px;              /* Ajoute de l’espace à l’intérieur des champs */
    font-size: 1.2em;           /* Agrandit la taille du texte pour une meilleure lisibilité */
    margin-bottom: 20px;        /* Ajoute un espace entre chaque champ */
    border: 1px solid #ccc;   /* Ajoute une bordure pour délimiter les champs */
    border-radius: 8px;         /* Arrondit les coins des champs */
}

/* Ajustement de la zone de texte*/
.contact textarea {
    height: 150px;              /* Augmente la hauteur du champ pour écrire des messages plus longs */
}

/* Bouton */
.contact input[type="submit"] {
    width: 100%;                           /* Le bouton prend toute la largeur disponible */
    padding: 15px;                         /* Ajoute de l’espace pour le rendre plus visible */
    font-size: 1.5em;                      /* Agrandit la taille du texte */
    font-weight: bold;                     /* Met le texte en gras */
    background-color: #0056b3;           /* Couleur bleue du bouton */
    color:#f4D7C8;                        /* Texte en blanc pour un bon contraste */
    border: none;                          /* Supprime les bordures par défaut */
    cursor: pointer;                       /* Change le curseur */
    border-radius: 8px;                    /* Arrondit les coins */
    transition: background 0.3s;           /* Ajoute une animation lors du survol */
}

/* EFFET DE SURVOL DU BOUTON */
.contact input[type="submit"]:hover {
    background-color: #b3d4ff; /* Change la couleur en bleu plus foncé au survol */
}
</style>

