<template>  
    <TheHeader />
<div class="error">
    <h1> ERROR 404</h1>
    <h4>Oh non ! Vous avez atteint le côté obscur du web. Revenez vers la lumière en utilisant le menu de navigation.</h4>
<img id="error-img" src="@/assets/images/ErrorPage/Error-meteor.jpeg" alt="image erreur 404, avec une météorite qui remplace le zéro">
</div>
<TheFooter />
    </template>
    
    <script setup>
    import TheHeader from '@/components/theHeader.vue';
    import TheFooter from '@/components/theFooter.vue';
    </script>
    
    <style scoped>
    .error{
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        width: 100%;
    }
    #error-img{
        width: 400px;
        border-radius: 50px;
    }
    </style>
    