<template>
  <header>
    <nav>
      <a href="#" title="Logo entreprise">
        <img id="logo" src="../assets/images/logoAntoineNoir.png" alt="Logo de l'entreprise, c'est écrit le prénom Antoine en noir, souligner avec un trait doré">
      </a>

      <ul>
        <li><a href="#">Présentation</a></li>
        <li><a href="#">Création</a></li>
        <li><a href="#">Contact</a></li>
      </ul>
    </nav>
  </header>

</template>
    
<script setup>
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
    