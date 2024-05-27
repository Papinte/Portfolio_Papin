<template>
  <div class="bloc-modale" v-if="reveleCv">
    <div class="overlay" v-on:click="toggleModale('cv')"></div>
    <div class="modale card">
      <div class="btn-modale btn btn-danger" v-on:click="toggleModale('cv')">
        X
      </div>
      <slot name="cv"></slot>
      <div class="modal-text">
        <h1>Mon CV en ligne</h1>
        <small>Créer le 03/04/2024</small>
        <p>Technologies utilisées : HTML & CSS</p>
        <p>
          <a href="https://github.com/Papinte/Curriculum-Vit-" target="_blank"
            >Le repository GitHub du cv</a
          >
        </p>
      </div>
    </div>
  </div>

  <div class="bloc-modale" v-if="reveleCdg">
    <div class="overlay" v-on:click="toggleModale('cdg')"></div>
    <div class="modale card">
      <div class="btn-modale btn btn-danger" v-on:click="toggleModale('cdg')">
        X
      </div>
      <slot name="cdg"></slot>
      <div class="modal-text">
        <h1>Cahier des charges</h1>
        <small>Créer le 10 avril 2024</small>
        <p>Technologies utilisées : Adobe InDesign</p>
        <p>
          <a
            href="../assets/images/Modale/cdg/Cahier-des charges-Antoine.pdf"
            download="cdg/Cahier-des charges-Antoine.pdf"
            target="_blank">Télécharger le PDF du cahier des charges</a>
        </p>
      </div>
    </div>
  </div>

  <div class="bloc-modale" v-if="reveleComment">
    <div class="overlay" v-on:click="toggleModale('comment')"></div>
    <div class="modale card">
      <div
        class="btn-modale btn btn-danger"
        v-on:click="toggleModale('comment')"
      >
        X
      </div>
      <slot name="comment"></slot>
      <div class="modal-text">
        <h1>Espace de commentaire</h1>
        <small>Créer le 06 mai 2024</small>
        <p>Technologies utilisées : JavaScript</p>
        <p>
          <a
            href="https://github.com/Papinte/comment-area"
            target="_blank">Le repository GitHub de l'espace commentaire</a>
        </p>
      </div>
    </div>
  </div>
</template>

<script setup>
import { defineProps } from "vue";

defineProps({
  reveleCv: Boolean,
  reveleCdg: Boolean,
  reveleComment: Boolean,
  toggleModale: Function,
});
</script>

<style scoped>
.modal-text {
  font-size: 1.3rem;
  padding: 20px;
  line-height: 50px;
}
a {
  text-decoration: none;
  color: black;
}
a:hover {
  color: gold;
}
h1 {
  text-align: center;
  border: 3px solid gold;
}

.bloc-modale {
  position: fixed;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 1;
}
.overlay {
  background: rgba(0, 0, 0, 0.5);
  position: fixed;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
}
.modale {
  background: white;
  color: black;
  padding: 50px;
  position: fixed;
  display: flex;
  flex-direction: row;
}
.btn-modale {
  position: absolute;
  top: 10px;
  right: 10px;
}
</style>
