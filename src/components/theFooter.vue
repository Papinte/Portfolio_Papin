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
                <small>Dernier mise à jour le <time datetime="2024-05-20">20/05/2024</time></small> 
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
}

#img-link {
        display: flex;
        flex-direction: row;
        justify-content: center;
        margin-top: 100px;

}
img{
        width: 40px;
        padding: 20px 20px 0 20px;
}
#update{
        display: flex;
        justify-content: center;
        color: black;
}

</style>