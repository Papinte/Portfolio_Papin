<template>
  <RouterView />
    <TheHeader />
    
  <main>
    <section class="banner">
      <!--Bannière-->
      <img
        class="banne__picture"
        src="@/assets/images/homePage/Web_dev_office.jpeg"
        title="Bannière"
        alt="Bannière avec des vagues de différente nuance de bleu"
      />
      <h1>ANTOINE PAPIN</h1>
      <h3>Développeur Web</h3>
    </section>

    <!--Bouton pour remonter en haut de la page-->
    <div>
      <button id="top-btn" title="Retour en haut">&#9650;</button>
    </div>

    <section class="present" id="presentation">
      <!--A propos-->
      <div class="present__text">
        <h2>Qui suis-je ?</h2>
        <p>
          Salut ! Je suis Antoine Papin, un développeur web junior avec une
          passion pour l'innovation et l'expérience utilisateur. Formé pendant
          un an au Centre Européen de Formation, j'ai obtenu mon Diplôme de
          titre professionnel en développement web et web mobile. Je me
          spécialise dans le front-end, où je mets en œuvre ma créativité pour
          façonner des interfaces web remarquables. Bienvenue dans mon monde
          numérique !
        </p>
      </div>
      <img
        id="profil-pic"
        src="@/assets/images/homePage/profil-black-white.png"
        title="Photo de profil"
        alt="Photo en noir et blanc d'un homme debout en t-shirt et short, face à la mer"
      />
    </section>
    <section id="concept">
      <h2>Mes projets</h2>
      <div class="projects">
        <div>
          <img
            class="projects__img"
            src="@/assets/images/homePage/CV_Antoine.png"
            title="Mon cv en ligne"
            alt="Image réduite d'un CV"
            v-on:click="toggleModale('cv')"
          />
          <p>Mon CV en ligne</p>

          <TheModale :reveleCv="reveleCv" :toggleModale="toggleModale">
            <template v-slot:cv>
              <div class="carousel" id="carousel-cv">
                
                  <button class="prev" @click="changeSlide(-1, 'carousel-cv')">
                    ❮
                  </button>
                  <div class="slides">
                  <img
                    class="modale-img"
                    src="@/assets/images/Modale/cv-ligne/CV_Antoine.png"
                    title="Mon cv en ligne"
                    alt="Image réduite d'un CV"
                  />
                  <img
                    class="modale-img"
                    src="@/assets/images/Modale/cv-ligne/CV_Antoine1.png"
                    title="Mon cv en ligne"
                    alt="Image réduite d'un CV"
                  />
                  <img
                    class="modale-img"
                    src="@/assets/images/Modale/cv-ligne/CV_Antoine2.png"
                    title="Mon cv en ligne"
                    alt="Image réduite d'un CV"
                  />
                  <img
                    class="modale-img"
                    src="@/assets/images/Modale/cv-ligne/CV_Antoine3.png"
                    title="Mon cv en ligne"
                    alt="Image réduite d'un CV"
                  />
                </div>
                  <button class="next" @click="changeSlide(1, 'carousel-cv')">
                    ❯
                  </button>
                
            </div>
            </template>
          </TheModale>
        </div>

        <div>
          <img
            class="projects__img"
            src="@/assets/images/homePage/CDG_Antoine.jpg"
            title="Mon cahier des charges"
            alt="Image réduite de la couverture d'un cahier des charges"
            v-on:click="toggleModale('cdg')"
          />
          <p>Un cahier des charges</p>
          <TheModale :reveleCdg="reveleCdg" :toggleModale="toggleModale">
            <template v-slot:cdg>
              <div class="carousel" id="carousel-cdg">
                <button class="prev" @click="changeSlide(-1, 'carousel-cdg')">
                  ❮
                </button>
                <div class="slides">
                  <img
                    class="modale-img"
                    src="@/assets/images/homePage/CDG_Antoine.jpg"
                    title="Mon cahier des charges"
                    alt="Image réduite de la couverture d'un cahier des charges"
                  />
                  <img
                    class="modale-img"
                    src="@/assets/images/Modale/cdg/CDG_page1.jpg"
                    alt="Page du cahier des charges"
                  />
                  <img
                    class="modale-img"
                    src="@/assets/images/Modale/cdg/CDG_page2.jpg"
                    alt="Page du cahier des charges"
                  />
                </div>
                <button class="next" @click="changeSlide(1, 'carousel-cdg')">
                  ❯
                </button>
              </div>
            </template>
          </TheModale>
        </div>

        <div>
          <img
            class="projects__img"
            src="@/assets/images/homePage/comment-area-index.png"
            title="Espace commentaire"
            alt="Image réduite d'une page de site internet, avec des commentaire et un formulaire à remplir pour mettre son commentaire"
            v-on:click="toggleModale('comment')"
          />
          <p>Un espace de commentaire dynamique</p>
          <TheModale
            :reveleComment="reveleComment"
            :toggleModale="toggleModale"
          >
            <template v-slot:comment>
              <div class="carousel" id="carousel-comment">
                <button
                  class="prev"
                  @click="changeSlide(-1, 'carousel-comment')"
                >
                  ❮
                </button>
                <div class="slides">
                  <img
                    class="modale-img"
                    src="@/assets/images/homePage/comment-area-index.png"
                    title="Espace commentaire"
                    alt="Image réduite d'une page de site internet, avec des commentaire et un formulaire à remplir pour mettre son commentaire"
                  />
                  <img
                    class="modale-img"
                    src="@/assets/images/Modale/comment-area/comment-area-index1.png"
                    title="Espace commentaire"
                    alt="Image du site, avec le commentaire dynamique"
                  />
                  <img
                    class="modale-img"
                    src="@/assets/images/Modale/comment-area/comment-area-index2.png"
                    title="Espace commentaire"
                    alt="Image du site, avec le commentaire dynamique"
                  />
                  <img
                    class="modale-img"
                    src="@/assets/images/Modale/comment-area/comment-area-index3.png"
                    title="Espace commentaire"
                    alt="Image du site, avec le commentaire dynamique"
                  />
                </div>
                <button
                  class="next"
                  @click="changeSlide(1, 'carousel-comment')"
                >
                  ❯
                </button>
              </div>
            </template>
          </TheModale>
        </div>
      </div>
    </section>

    <section>
      <img
        id="background-form"
        src="@/assets/images/homePage/fond_input.jpeg"
        title="Background du formulaire"
        alt="Fond de page stylisé avec des taches gris et des courbes"
      />

      <form id="contact" class="form-style" v-on:submit.prevent="submitForm">
        <h2>Contactez moi</h2>

        <!--Message d'erreur-->

        <div id="openMessageEnvoi" v-if="openMessageEnvoi">
          <h5>&#10060; Tous les champs doivent être remplis</h5>
        </div>
        <div id="confirmationMessage" v-if="confirmationMessage">
          <h5>{{ confirmationMessage }}</h5>
        </div>

        <input type="text" v-model="nom" placeholder="Nom" />

        <input type="text" v-model="prenom" placeholder="Prénom" />

        <input type="text" v-model="objet" placeholder="Objet" />

        <textarea
          v-model="message"
          cols="30"
          rows="10"
          placeholder="Message"
        ></textarea>

        <button id="bouton" type="submit">Envoyer</button>
      </form>
    </section>
  </main>
  <theFooter/>
  <RouterLink to="/">Accueil</RouterLink>
  <RouterLink to="/about">Erreur 404</RouterLink>
</template>

<script setup>
import TheHeader from "@/components/theHeader.vue";
import theFooter from "@/components/theFooter.vue";

import { ref, reactive } from "vue";
import TheModale from "@/components/TheModale.vue";

const slideIndices = reactive({
  "carousel-cv": 0,
  "carousel-cdg": 0,
  "carousel-comment": 0,
});

function changeSlide(n, carouselId) {
  const carousel = document.getElementById(carouselId);
  const slides = carousel.querySelectorAll(".slides img");
  let newIndex = slideIndices[carouselId] + n;

  if (newIndex >= slides.length) {
    newIndex = 0;
  }
  if (newIndex < 0) {
    newIndex = slides.length - 1;
  }

  slideIndices[carouselId] = newIndex;

  const offset = -newIndex * 100;
  carousel.querySelector(".slides").style.transform = `translateX(${offset}%)`;
}

//Afficher les différentes modales
const reveleCv = ref(false);
const reveleCdg = ref(false);
const reveleComment = ref(false);

function toggleModale(modale) {
  if (modale === "cv") {
    reveleCv.value = !reveleCv.value;
  } else if (modale === "cdg") {
    reveleCdg.value = !reveleCdg.value;
  } else if (modale === "comment") {
    reveleComment.value = !reveleComment.value;
  }
}

//Code pour le formulaire
const prenom = ref("");
const nom = ref("");
const objet = ref("");
const message = ref("");
const openMessageEnvoi = ref(false);
const confirmationMessage = ref("");

const submitForm = (event) => {
  event.preventDefault(); // Empêcher le comportement par défaut du formulaire

  // Vérifier que tous les champs sont remplis
  if (!prenom.value || !nom.value || !objet.value || !message.value) {
    openMessageEnvoi.value = true; // Afficher le message d'erreur
    return; // Arrêter l'exécution de la fonction
  }

  // Soumettre le formulaire et construire le message de confirmation
  confirmationMessage.value = `Bonjour ${nom.value} ${prenom.value}! Votre message "${objet.value}" a été envoyé avec succès.`;
  openMessageEnvoi.value = false; // Ne pas afficher le message d'erreur

  // Simuler l'envoi de l'email ici, puis effacer le formulaire
  clearForm();
};

const clearForm = () => {
  // Effacer les champs du formulaire et le message de confirmation
  prenom.value = "";
  nom.value = "";
  objet.value = "";
  message.value = "";
};

//Code pour le bouton pour remonter la page
// s'assurer que le script JavaScript s'exécute seulement après que le document HTML
document.addEventListener("DOMContentLoaded", function () {
  // Sélectionne le bouton
  const topBtn = document.getElementById("top-btn");

  // Ajoute un écouteur d'événements sur le défilement de la fenêtre
  window.addEventListener("scroll", function () {
    // Vérifie la position de défilement de la page
    if (window.scrollY > 200) {
      topBtn.style.display = "block";
    } else {
      topBtn.style.display = "none";
    }
  });

  // Ajoute un écouteur d'événements pour le clic sur le bouton
  topBtn.addEventListener("click", function () {
    // Fonction pour faire défiler vers le haut
    window.scrollTo({ top: 0, behavior: "smooth" });
  });
});
</script>

<style scoped>

/*Code carrousel d'image et modale*/

.slides-text {
  display: flex;
  justify-content: space-between;
}

.modale-img {
  object-fit: cover;
  width: 400px;
  height: 100%;
  transition: transform 0.25s ease;
}

.modale-img:hover {
  transform: scale(1.2);
}

.carousel {
  position: relative;
  width: 100%;
  max-width: 400px;
  margin: auto;
  overflow: hidden;
}

.slides {
  display: flex;
  transition: transform 0.5s ease-in-out;
}

.prev {
  left: 0;
  position: absolute;
  top: 50%;
  background-color: rgba(0, 0, 0, 0.5);
  color: white;
  border: none;
  padding: 10px;
  cursor: pointer;
  z-index: 1;
}

.next {
  right: 0;
  position: absolute;
  top: 50%;
  background-color: rgba(0, 0, 0, 0.5);
  color: white;
  border: none;
  padding: 10px;
  cursor: pointer;
}

/* Début de code pour la bannière et les titres*/
.banner {
  display: flex;
  flex-direction: column;
  align-items: center;
  font-size: 4rem;
  color: white;
  margin: 50px 50px 150px 50px;
  

}

.banner h1 {
  padding: 0 50px 0 50px;
  border: solid 1px gold;
  box-sizing: border-box;
  margin-top: 70px;
  font-size: 1.2em;
}

h3 {
  font-size: 0.8em;
  border-bottom: 2px solid gold;
}

.banne__picture {
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
.present {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
  background-color: rgb(228, 228, 228);
  margin: 70px;
  padding: 30px;
  font-size: 1.3rem;
}

.present__text {
  box-sizing: border-box;
  width: 500px;
}
.present__text h2 {
  border-bottom: solid 2px gold;
}

#profil-pic {
  width: 500px;
  border-radius: 50%;
}
/* Fin de code pour la photo de profil et la présentation*/

/*Debut de code pour l'importation des projets */
.projects {
  display: flex;
  flex-direction: row;
  justify-content: space-around;
  margin: 50px 0 50px 0;
  padding: 30px 0 30px 0;
}
.projects__img {
  width: 300px;
  height: 300px;
  object-fit: cover;
  filter: brightness(80%);
  border-radius: 25%;
}
.projects__img:hover {
  filter: brightness(100%);
  box-shadow: 3px 3px;
  cursor: pointer;
}
.projects p{
    text-align: center;
}
.projects a {
  text-decoration: none;
  text-align: center;
  color: black;
}
/*Fin de code pour l'importation des projets */

/*Message d'erreur*/
#openMessageEnvoi {
  display: flex;
  background-color: rgb(255, 154, 154);
  width: fit-content;
  margin: auto;
  padding: 0 5px 0 5px;
  border-radius: 10px;
}
/*Message de succes*/
#confirmationMessage {
  display: flex;
  background-color: rgb(163, 255, 145);
  width: fit-content;
  margin: auto;
  padding: 0 5px 0 5px;
  border-radius: 10px;
}

/*Debut de code du formulaire */
#background-form {
  position: absolute;
  left: 0;
  width: 100%;
  height: auto;
  max-height: 700px;
  z-index: -1;
  filter: brightness(70%);
  opacity: 90%;
}

.form-style {
  display: flex;
  flex-direction: column;
  margin: auto;
  width: 500px;
  height: auto;
  font-size: 1.2rem;
}

.form-style h2 {
    margin-top: 20px;
    text-align: center;
    border: 3px solid gold;
    border-radius: 10px;
    color: white;
}
.form-style input {
  border: none;
  background: rgb(235, 235, 235);
  margin: 20px;
  font-size: 1em;
  border-radius: 5px;
}

.form-style textarea {
  border: none;
  border-bottom: 1px solid grey;
  background: rgb(235, 235, 235);
  margin: 20px;
  font-size: 1em;
  border-radius: 5px;
}
#bouton {
  margin-top: 10px;
  background-color: gold;
  color: black;
  align-self: flex-end;
  border: none;
  border-radius: 10px;
  padding: 5px 10px 5px 10px;
  font-size: 1em;
}
#bouton:hover {
  cursor: pointer;
}
/*Fin de code du formulaire */

/*style du bouton pour remonter en haut de la page*/
#top-btn {
  display: none;
  position: fixed;
  bottom: 20px;
  right: 20px;
  background-color: gold;
  color: black;
  border-radius: 50%;
  padding: 10px;
}
</style>
