<template>
    <div class="presentation">
        <section id="je-suis" class="presentation-container">
            <img src="../assets/img-portfolio/photo.jpg" alt="Ma photo" class="photo-profil" width="150" height="150"/>
            <div class="contenu">
                <h3>Qui suis-je ?</h3>
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
    </div>
</template>


<style scoped>
h3 {
    color: #D9D9D9;
    font-size: 2em; /* Augmente la taille du titre */
    font-weight: bold;
    text-align: center; /* Centre le titre */ 
    margin-top: 15px; /* Espacement entre l’image et le titre */
}

.presentation {
    display: flex;
    flex-direction: column;
    align-items: center; /* Centre tout le contenu */
    text-align: center;
    max-width: 1100px;
    font-size: 1em;
}

.presentation-container {
    display: flex;
    flex-direction: column;
    align-items: center; /* Centre horizontalement */
    justify-content: center;
    text-align: center;
    padding: 20px;
    box-sizing: border-box;
    font-size: 1.5em;
}

.photo-profil {
    border-radius: 50%;
    height: auto;
}

.contenu {
    line-height: 1.8; /* Améliore la lisibilité */
    text-align: center; /* Centre le texte sous l'image */
}
</style>
