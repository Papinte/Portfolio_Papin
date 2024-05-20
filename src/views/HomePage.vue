<template>
    <theHeader />
    <main>
        <section class="banner">
            <!--Bannière-->
            <img class="banne__picture" src="@/assets/images/homePage/Web_dev_office.jpeg" title="Bannière" alt="Bannière avec des vagues de différente nuance de bleu">
            <h1>ANTOINE PAPIN</h1>
            <h5>Développeur Web</h5>
        </section>

        <section class="about" ref="presentation">
            <!--A propos-->
            <div class="about__text">
                <h2>Qui suis-je ?</h2>
                <p>Salut ! Je suis Antoine Papin, 
                    un développeur web junior avec une passion pour 
                    l'innovation et l'expérience utilisateur. 
                    Formé pendant un an au Centre Européen de Formation, 
                    j'ai obtenu mon Diplôme de titre professionnel en développement web et web mobile. 
                    Je me spécialise dans le front-end, où je mets en œuvre ma créativité pour façonner des interfaces web 
                    remarquables. Bienvenue dans mon monde numérique !</p>
            </div>
            <img id="profil-pic" src="@/assets/images/homePage/profil-black-white.png" title="Photo de profil" alt="Photo en noir et blanc d'un homme debout en t-shirt et short, face à la mer">
        </section>

        <section>
            <h2>Mes projets</h2>
            <div class="projects">
                <a href="#">
                    <img class="projects__img" src="@/assets/images/homePage/CV_Antoine.png" title="Mon cv en ligne" alt="Image réduite d'un CV">
                    <p>Voici mon CV en ligne</p>
                </a>

                <a href="#">
                    <img class="projects__img" src="@/assets/images/homePage/CDG_Antoine.jpg" title="Mon cahier des charges" alt="Image réduite de la couverture d'un cahier des charges">
                    <p>Voici mon cahier des charges</p>
                </a>

                <a href="#">
                    <img class="projects__img" src="@/assets/images/homePage/comment-area-index.png" title="Espace commentaire" alt="Image réduite d'une page de site internet, avec des commentaire et un formulaire à remplir pour mettre son commentaire">
                    <p>Un espace de commentaire dynamique</p>
                </a>
            </div>
    </section>
    <section>
        <img id="background-form" src="@/assets/images/homePage/fond-753159.jpeg" title="Background du formulaire" alt="Fond de page stylisé avec des taches gris et des courbes">
        
            <form class="form-style" action="#" method="post">

                <h2>Contactez moi</h2>

                <input type="text" name="nom" id="nom" placeholder="Nom">

                <input type="text" name="prenom" id="prenom" placeholder="Prénom">

                <input type="text" name="Objet" id="objet" placeholder="Objet">

                <textarea name="message" id="message" cols="30" rows="10" placeholder="Message"></textarea>

                <button id="btn" type="submit">Envoyer</button>
            </form>
    </section>
</main>
<theFooter />

</template>

<script setup>
    import theHeader from '@/components/theHeader.vue';
    import theFooter from '@/components/theFooter.vue';

</script>

<style scoped>
    /* importation de la police pour l'ensemble de la page */
main{
    font-family: "Titillium web";
    width: 100%;
}
    
    

    /* Début de code pour la bannière et les titres*/ 
.banner{
    display: flex;
    flex-direction: column;
    align-items: center;
    font-size: 3rem;
    color: white;
    margin: 50px
}

.banner h1{
    padding: 0 50px 0 50px;
    border: solid 1px gold;
    box-sizing: border-box;
    width: auto;
}

h5{
    border-bottom: 2px solid gold;
}

.banne__picture{
    position: absolute; /* Position absolue pour la photo */
    top: 0;
    left: 0; /* position horizontale de la photo */
    width: 100%; /* Pour que la largeur de la photo s'adapte à la largeur du main */
    z-index: -1; /*la photo est en arrière-plan par rapport au contenu du main */
    height: auto;
    max-height: 500px;
    filter: brightness(10%);
    opacity: 85%;

}
    /* Fin de code pour la bannière et les titres*/ 

    /* Début de code pour la photo de profil et la présentation*/ 
.about{
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    background-color: rgb(228, 228, 228);
    margin: 70px 70px 0 70px;
    padding: 30px;
    font-size: 1.3rem;
}

.about__text{
    box-sizing: border-box;
    width: 500px;     
}
.about__text h2{
    border-bottom: solid 2px gold;
}

#profil-pic{
    width: 500px;
    height: auto;
    border-radius: 50%;
}
    /* Fin de code pour la photo de profil et la présentation*/ 

    /*Debut de code pour l'importation des projets */
.projects{
    display: flex;
    flex-direction: row;
    justify-content: space-around;
    margin: 50px 0 50px 0;

    padding: 30px 0 30px 0;
        
}
.projects__img{
    width: 300px;
    height: 300px;
    object-fit: cover;
    filter: brightness(80%);
    border-radius: 25%;
}
    /*Fin de code pour l'importation des projets */

#background-form{
    position: absolute;
    left: 0;
    width: 100%;
    height: auto;
    max-height: 700px;
    z-index: -1;
    object-fit: cover;
    opacity: 70%;
}

.form-style{
    display: flex;
    flex-direction: column;
    margin: auto;
    width: 500px;
    height: auto;
    font-size: 1.2rem;
}

.form-style h2{
    text-align: center;
    border: 3px solid gold;
    border-radius: 10px
}
.form-style input{
    border: none;
    background: rgb(235, 235, 235);
    margin: 20px;
    font-size: 1em;
    box-shadow: 3px 3px 10px grey;
}

.form-style textarea{
    border: none;
    border-bottom: 1px solid grey;
    background: rgb(235, 235, 235);
    margin: 20px;
    font-size: 1em;
    box-shadow: 3px 3px 10px grey;
}
button{
    margin-top: 10px;
    background-color: black;
    color: white;
    align-self: flex-end;
    border: none;
    border-radius: 10px;
    padding: 5px 10px 5px 10px;
    font-size: 1em;
    box-shadow: 3px 3px 10px grey;
}

</style>
