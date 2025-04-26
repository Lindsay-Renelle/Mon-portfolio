<template>
        <section id="contact"  class="contact">
            <h2>Contactez-moi</h2>
            <form>
                <input type="text" placeholder="Nom">
                <input type="email" placeholder="Email">
                <textarea placeholder="Message"></textarea>
                <input type="submit" value="Envoyer">
            </form>
        </section>
</template>


<style scoped>
h2 {
    font-size: 2em; /* Augmente la taille du titre */
    font-weight: bold;
    text-align: center; /* Centre le titre */
    width: 100%;
    margin-top: 15px; /* Espacement entre l’image et le titre */
}

.contact {
  margin : auto;
  padding-top: 30px;
}

/* SECTION FORMULAIRE */
.contact form {
    display: flex; /* Utilisation de flexbox pour aligner les éléments */
    flex-direction: column; /* Met les éléments en colonne */
    align-items: center; /* Centre les éléments horizontalement */
    width: 80%; /* Le formulaire prend 80% de la largeur disponible */
    max-width: 500px; /* Évite qu'il devienne trop large sur les grands écrans */
    margin: 0 auto; /* Centre le formulaire dans la page */
}

/* CHAMPS DE TEXTE ET ZONE DE MESSAGE */
.contact input, 
.contact textarea {
    width: 100%; /* Prend toute la largeur disponible */
    padding: 15px; /* Ajoute de l’espace à l’intérieur des champs pour un meilleur confort */
    font-size: 1.2em; /* Agrandit la taille du texte pour une meilleure lisibilité */
    margin-bottom: 20px; /* Ajoute un espace entre chaque champ */
    border: 1px solid #ccc; /* Ajoute une bordure grise claire pour bien délimiter les champs */
    border-radius: 8px; /* Arrondit légèrement les coins des champs */
}

/* AJUSTEMENT SPÉCIFIQUE DE LA ZONE DE TEXTE */
.contact textarea {
    height: 150px; /* Augmente la hauteur du champ pour écrire des messages plus longs */
}

/* BOUTON D'ENVOI */
.contact input[type="submit"] {
    width: 100%; /* Le bouton prend toute la largeur disponible */
    padding: 15px; /* Ajoute de l’espace pour le rendre plus visible et facile à cliquer */
    font-size: 1.2em; /* Agrandit la taille du texte */
    font-weight: bold; /* Met le texte en gras */
    background-color: #007bff; /* Couleur bleue du bouton */
    color: white; /* Texte en blanc pour un bon contraste */
    border: none; /* Supprime les bordures par défaut */
    cursor: pointer; /* Change le curseur en une main pour indiquer que c'est cliquable */
    border-radius: 8px; /* Arrondit les coins du bouton */
    transition: background 0.3s; /* Ajoute une animation fluide lors du survol */
}

/* EFFET DE SURVOL DU BOUTON */
.contact input[type="submit"]:hover {
    background-color: #0056b3; /* Change la couleur en bleu plus foncé au survol */
}
</style>

