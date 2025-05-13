<template>
    <div class="competences">
        <section id="competences" class="competences-container">
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
    </div>
</template>


<style scoped>
h2 {
    color: #A8C5E6;
    font-family: 'Lobster'; /*Police*/
    font-size: 2em; /* Augmente la taille du titre */
    font-weight: bold;
    text-align: center; /* Centre le titre */ 
    margin-top: 15px; /* Espacement entre l’image et le titre */
}

.competences {
    display: flex;
    flex-direction: column;
    justify-content: center;
    margin: 0 auto;
}

.competences-container {
    line-height: 2; /* Améliore la lisibilité */
    text-align:center; /* Centre le texte sous l'image */
    margin: 0 auto; 
}

.competences-container p {
   font-size: 1.5em;
    margin-bottom: 20px;
    text-align: center;
}

.competences-container ul {
    list-style: none; /* Supprime les points */
    line-height: 1.8; /* Améliore la lisibilité */
    text-align:center; /* Centre le texte sous l'image */
    font-size: 1.5em;
    padding: 0;
    margin: 0 auto;
    width: fit-content;/*Ajuste la largeur du bloc*/
}
</style>