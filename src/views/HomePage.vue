<template>
    <theHeader />
    <main>
        <TheModale v-bind:revele="revele" :toggleModale="toggleModale"></TheModale>
        <div v-on:click="toggleModale" class="btn-modale"></div>
        <section class="banner">
            <!--Bannière-->
            <img class="banne__picture" src="@/assets/images/homePage/Web_dev_office.jpeg" title="Bannière" alt="Bannière avec des vagues de différente nuance de bleu">
            <h1>ANTOINE PAPIN</h1>
            <h5>Développeur Web</h5>
        </section>

        <!--Bouton pour remonter en haut de la page-->
        <div>
            <button id="top-btn" title="Retour en haut">&#9650;</button>
        </div>

        <section class="present" id="presentation">
            <!--A propos-->
            <div class="present__text">
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

        <section id="concept">
            <h2>Mes projets</h2>
            <div class="projects">
                <a href="#">
                    <img class="projects__img" src="@/assets/images/homePage/CV_Antoine.png" title="Mon cv en ligne" alt="Image réduite d'un CV" v-on:click="toggleModale">
                    <p>Mon CV en ligne</p>
                </a>

                <a href="#">
                    <img class="projects__img" src="@/assets/images/homePage/CDG_Antoine.jpg" title="Mon cahier des charges" alt="Image réduite de la couverture d'un cahier des charges" v-on:click="toggleModale">
                    <p>Un cahier des charges</p>
                </a>

                <a href="#">
                    <img class="projects__img" src="@/assets/images/homePage/comment-area-index.png" title="Espace commentaire" alt="Image réduite d'une page de site internet, avec des commentaire et un formulaire à remplir pour mettre son commentaire" v-on:click="toggleModale">
                    <p>Un espace de commentaire dynamique</p>
                </a>
            </div>
    </section>

    <section>
        <img id="background-form" src="@/assets/images/homePage/fond_input.jpeg" title="Background du formulaire" alt="Fond de page stylisé avec des taches gris et des courbes">
        
        <!--Message d'erreur-->

            <form id="contact" class="form-style" method="post">

                <h2>Contactez moi</h2>
                <div id="error-message">
            <h3> &#10060; Tous les champs doivent être remplis</h3>
        </div>
        <div id="success-message">
            <h3> &#10004; Votre message a bien été envoyé !</h3>
        </div>

                <input type="text" name="nom" id="last-name" placeholder="Nom">

                <input type="text" name="prenom" id="first-name" placeholder="Prénom">

                <input type="text" name="Objet" id="objet" placeholder="Objet">

                <textarea name="message" id="message" cols="30" rows="10" placeholder="Message"></textarea>

                <button id="bouton" type="submit">Envoyer</button>
            </form>
    </section>
</main>
<theFooter />

</template>

<script setup>
    import theHeader from '@/components/theHeader.vue';
    import theFooter from '@/components/theFooter.vue';
    
    import { ref } from 'vue';
    import TheModale from '@/components/Modale.vue';

    const revele = ref(false);
    const toggleModale = () => {
    revele.value = !revele.value;
    }
    // s'assurer que le script JavaScript s'exécute seulement après que le document HTML
    document.addEventListener('DOMContentLoaded', function() {
      // Sélectionne le bouton
      const topBtn = document.getElementById('top-btn');

      // Ajoute un écouteur d'événements sur le défilement de la fenêtre
      window.addEventListener('scroll', function() {
        // Vérifie la position de défilement de la page
        if (window.scrollY > 200) {
          topBtn.style.display = 'block';
        } else {
          topBtn.style.display = 'none';
        }
      });

      // Ajoute un écouteur d'événements pour le clic sur le bouton
      topBtn.addEventListener('click', function() {
        // Fonction pour faire défiler vers le haut
        window.scrollTo({top: 0, behavior: 'smooth'});
      });
    });

    document.addEventListener('DOMContentLoaded', function() {
        function fieldcheck() {
        let inputLastName = document.getElementById("last-name");
        let inputFirstName = document.getElementById("first-name");
        let inputObjet = document.getElementById("objet");
        let inputMessage = document.getElementById("message");

        const errorMessage =  document.getElementById("error-message");
        if (inputLastName.value === "" || inputFirstName.value === "" || inputObjet.value === "" || inputMessage.value === ""){
            errorMessage.style.display = "block";
            return false;
        } else {
            errorMessage.style.display = "none";
            return true;
        }
    }

    function leaveMail() {
        const successMessage = document.getElementById("success-message");

        if(fieldcheck()) {
        successMessage.style.display = "block";
        }

    }
    const submitButton = document.getElementById("bouton");
    submitButton.addEventListener("click", function(event) {
        event.preventDefault(); 
        if(fieldcheck()) {
            leaveMail();

        // Effacer les champs des inputs
        document.getElementById("last-name").value = "";
        document.getElementById("first-name").value = "";
        document.getElementById("objet").value = "";
        document.getElementById("message").value = "";
        }
    })
    })
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
.present{
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    background-color: rgb(228, 228, 228);
    margin: 70px 70px 0 70px;
    padding: 30px;
    font-size: 1.3rem;
}

.present__text{
    box-sizing: border-box;
    width: 500px;     
}
.present__text h2{
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
.projects__img:hover{
    filter: brightness(100%);
    box-shadow: 3px 3px;
}

.projects a{
    text-decoration: none;
    text-align: center;
    color:black;
}
/*Fin de code pour l'importation des projets */

/*Message d'erreur*/
#error-message{
    display: flex;
    background-color: rgb(255, 154, 154);
    width: fit-content;
    margin: auto;
    padding: 0 10px 0 10px;
    border-radius: 10px;
    display: none;
}
/*Message de succes*/
#success-message{
    display: flex;
    background-color: rgb(163, 255, 145);
    width: fit-content;
    margin: auto;
    padding: 0 10px 0 10px;
    border-radius: 10px;
    display: none;
}

/*Debut de code du formulaire */
#background-form{
    position: absolute;
    left: 0;
    width: 100%;
    height: auto;
    max-height: 700px;
    z-index: -1;
    filter: brightness(70%);
    opacity: 90%;
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
    border-radius: 10px;
    color: white;
}
.form-style input{
    border: none;
    background: rgb(235, 235, 235);
    margin: 20px;
    font-size: 1em;
    border-radius: 5px
}

.form-style textarea{
    border: none;
    border-bottom: 1px solid grey;
    background: rgb(235, 235, 235);
    margin: 20px;
    font-size: 1em;
    border-radius: 5px
}
#bouton{
    margin-top: 10px;
    background-color: gold;
    color: black;
    align-self: flex-end;
    border: none;
    border-radius: 10px;
    padding: 5px 10px 5px 10px;
    font-size: 1em;
}
#bouton:hover{
    cursor: pointer;
}
/*Fin de code du formulaire */

/*style du bouton pour remonter en haut de la page*/
#top-btn{
    display: none;
    position: fixed;
    bottom: 20px;
    right: 20px;
    background-color: gold;
    color: black;
    border: none;
    border-radius: 50%;
    padding: 10px;
    cursor: pointer;
}

</style>
