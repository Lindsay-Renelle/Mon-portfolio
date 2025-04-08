<template>
    <div class="container">
        <section class="presentation">
                <img src="../assets/img-portfolio/photo.jpg" alt="Ma photo" class="photo-profil"/>
                <div class="contenu">
                    <h2>Qui suis-je ?</h2>
                    <p>Passionnée par le web et la technologie, je suis actuellement en formation pour devenir développeuse web. À 55 ans,
                        j'ai choisi de me reconvertir après une carrière enrichissante en tant qu'auxiliaire de vie à domicile.
                        Ce métier m'a permis de développer des qualités essentielles : l'écoute, la patience, l'empathie et une grande capacité d'adaptation.<br/>
                    </p>

                    <p>Aujourd'hui, je mets cette expérience humaine au service de ma nouvelle passion :
                        le développement web. Créer, résoudre des problèmes, et donner vie à des projets numériques est devenu pour moi une source d'épanouissement incroyable. 
                        Cette reconversion est bien plus qu'un défi professionnel, c'est un rêve devenu réalité.<br/>
                    </p>

                    <p>Curieuse et déterminée, j'apporte un regard unique et mature à mes projets,
                        tout en continuant à apprendre et à me perfectionner chaque jour. Je suis animée par le désir de concevoir des solutions innovantes, accessibles et utiles à tous.
                    </p>
             </div>  
        </section>

        <section class="competences">
            <h2>Mes compétences</h2>
            <p>Actuellement en formation en développement web, j'ai déjà acquis certaines compétences </p>
            <ul>
                <li>Html 5 - Débutant</li>
                <li>Css - Débutant</li>
                <li>GitHub - Débutant</li>
                <li>JavaScript - Débutant</li>
                <li>Framework - Débutant</li>
                <li>Bureautique - Intermédiaire</li>
                <li>Informatique - Intermédiaire</li>
            </ul>
        </section>

        <section class="projets">
            <h2>Mes projets</h2>
            <a href="../assets/img-portfolio/Img-cv-html.png"><img src="../assets/img-portfolio/Img-visuel-cv.png" alt="Image CV" class="cv"></a>
            <a href="../assets/document-pdf/Cahiers des Charges.pdf"><img src="../assets/img-portfolio/Cahier des charges 1.png" alt="Cahier des charges" class="cahier"></a>
            <a href="../assets/img-portfolio/Img-html-site-1.png"> <img src="../assets/img-portfolio/Img-visuel-site-1.png" alt="Coeur à prendre" class="coeur"></a>
        </section>

        <section class="contact">
            <h2>Contactez-moi</h2>
            <form>
                <input type="text" placeholder="Nom">
                <input type="email" placeholder="Email">
                <textarea placeholder="Message"></textarea>
                <input type="submit" value="Envoyer">
            </form>
        </section>
    </div> 
</template>


<style scoped>
.container {
    display: flex;
    flex-direction: column;
    align-items: center; /* Centre tout le contenu */
    text-align: center;
    max-width: 1200px;
    width: 100%;
    margin: 0 auto;
    font-size: 20px;
}

h2 {
    font-size: 2em; /* Augmente la taille du titre */
    font-weight: bold;
    text-align: center; /* Centre le titre */
    width: 100%;
    margin-top: 15px; /* Espacement entre l’image et le titre */
}

.presentation {
    display: flex;
    flex-direction: column;
    align-items: center; /* Centre horizontalement */
    justify-content: center;
    text-align: center;
    padding: 20px;
    box-sizing: border-box;
}

.photo-profil {
    width: 200px;
    height: auto;
    border-radius: 15%;
}

.contenu {
    line-height: 1.8; /* Améliore la lisibilité */
    text-align:center; /* Centre le texte sous l'image */
}

.contenu p {
    line-height: 2; /* Augmente l'espacement entre les lignes */
    text-align:center ;
    margin-bottom: 20px;
}

.contenu p:last-of-type {
    margin-bottom: 0; /* Supprime l’espace sous le dernier paragraphe */
}

.competences {
    line-height: 2; /* Améliore la lisibilité */
    text-align:center; /* Centre le texte sous l'image */
    margin: 0 auto;
}

.competences p {
    margin-bottom: 20px;
}
.competences ul {
    list-style: none; /* Supprime les points */
}

.projet {
    display: flex;
    flex-wrap: wrap; /* Permet aux images de passer à la ligne si l’écran est trop petit */
    justify-content: center; /* Centre les images horizontalement */
    gap: 20px; /* Ajoute un espacement entre les images */
}

.cv, .cahier, .coeur {
    width: 30%; /* Réduit la taille */
    height: auto;
    margin: 10px; /* Ajoute un espace autour des images */
}

main.contenu-principal {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  width: 100%;
  padding-top: 120px; /* Évite qu'il soit caché sous le header */
}

.presentation, .competences, .projets, .contact {
    margin-bottom: 80px; /* Assure un espacement constant */
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