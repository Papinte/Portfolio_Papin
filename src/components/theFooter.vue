<template>
    <footer>
        <div id="img-link">
            <a href="https://fr.linkedin.com/" title="linkedin" target="_blank">
                <img src="../assets/images/theFooter/linkedin.png" alt="Logo du réseau social Linkedin">
            </a>
            <a href="https://github.com/Papinte" title="Github" target="_blank">
                <img src="@/assets/images/theFooter/github.png" alt="Logo du gestionnaire de version github">
            </a>
            <a href="https://twitter.com/" title="twitter" target="_blank">
                <img src="../assets/images/theFooter/twitter.png" alt="Logo du réseau social X">
            </a>
        </div>
        <div id="update">
            <p>
                <small>Dernier mise à jour le <time datetime="2024-05-27">27/05/2024</time></small> 
            </p>
        </div>
    </footer>

</template>

<script setup>

</script>

<style scoped>
footer{
    width: 100%;
    font-family: "Titillium web";
    background-color: #FFFFE0;
    margin-top: 25px;

}

#img-link {
    display: flex;
    flex-direction: row;
    justify-content: space-around;
    margin: 0px 500px 0 500px;
    padding-top: 20px;

}
img{
    width: 30px;

}
#update{
    display: flex;
    justify-content: center;
    color: black;
}

</style>