<template>
        <div class="bloc-modale-cv" v-if="revele">

            <div class="overlay" v-on:click="toggleModale"></div>

            <div class="modale card">
                <div v-on:click="toggleModale" class="btn-modale btn btn-danger">X</div>

                <div id="curriculum">
                <img src="@/assets/images/Modale/cv-ligne/CV_Antoine.png" alt="Mon Cv en entier">
                <div id="cv-text">
                    <h2>Mon CV en ligne</h2>
                    <p>03 avril 2024</p>
                    <h5>Technologies utilisées :</h5>
                    <p>HTML & CSS</p>
                    <h5>Liens utiles :</h5>
                    <p>Cliquez <a href="https://github.com/Papinte/Curriculum-Vit-" target="_blank"> ici</a> pour visiter mon GitHub</p>
                </div>
                </div>
            </div>
        </div>

</template>

<script>


export default {
    name:'ModaleContent',
    props:['revele', 'toggleModale',]
}


</script>

<style scoped>
.bloc-modale-cv{
    position: fixed;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
}

.overlay{
    background: rgba(0, 0, 0, 0.5);
    position: fixed;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
}
.modale{
    background: #d6d6d6;
    color: black;
    padding: 50px;
    display: flex;
    flex-direction: row;
}

.btn-modale{
    position: absolute;
    top: 10px;
    right: 10px;
}

#curriculum{
    display: flex;
    flex-direction: row;

}

#curriculum img{
    width: 400px;
    transition: transform .1s;
    margin: 0 50px 0 0;
}
#curriculum img:hover{
    cursor: zoom-in;
    transform: scale(1.2);
}

#curriculum a{
    text-decoration: none;
    color: gold;
}
#curriculum h2{

    text-decoration: underline;
    text-decoration-color: gold;
}

</style>