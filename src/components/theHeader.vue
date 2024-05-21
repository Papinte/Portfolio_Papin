<template>
  <header>
    <nav>
        <img id="logo" src="../assets/images/logoAntoineNoir.png" alt="Logo de l'entreprise, c'est écrit le prénom Antoine en noir, souligner avec un trait doré">

      <ul>
        <li><a href="#presentation" id="scroll-link-presentation">Présentation</a></li>
        <li><a href="#concept" id="scroll-link-concept">Créations</a></li>
        <li><a href="#contact" id="scroll-link-contact">Contact</a></li>
      </ul>
    </nav>
  </header>

</template>
    
<script setup>
import { onMounted } from 'vue';

onMounted(() => {
  const scrollLinkPresentation = document.getElementById('scroll-link-presentation');
  const scrollLinkConcept = document.getElementById('scroll-link-concept');
  const scrollLinkContact = document.getElementById('scroll-link-contact');

  if (scrollLinkPresentation) {
    scrollLinkPresentation.addEventListener('click', function(event){
      event.preventDefault();
      document.querySelector('#presentation').scrollIntoView({
        behavior: 'smooth'
      });
    });
  }

  if (scrollLinkConcept) {
    scrollLinkConcept.addEventListener('click', function(event){
      event.preventDefault();
      document.querySelector('#concept').scrollIntoView({
        behavior: 'smooth'
      });
    });
  }

  if (scrollLinkContact) {
    scrollLinkContact.addEventListener('click', function(event){
      event.preventDefault();
      document.querySelector('#contact').scrollIntoView({
        behavior: 'smooth'
      });
    });
  }
});
</script>
    
<style scoped>
header {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100vh;
}
nav{
  display: flex;
  flex-direction: row;
  background-color: #FFFFE0;
  padding: 5px 0 20px 0;

}

#logo{
  width: 100px;
  height: auto;
  margin: 10px 0 0 50px;
}

ul {
  width: 100%;
  display: flex;
  flex-direction: row;
  margin: auto;
  justify-content: space-around;
  list-style-type: none;
  font-size: 1.3rem;
}

a{
  font-family: "Titillium web";
  text-decoration: none;
  color: black;
}
a:hover{
  color: gold;
}

</style>
    