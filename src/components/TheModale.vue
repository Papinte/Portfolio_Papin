<template>

<div class="bloc-modale" v-if="reveleCv">
    <div class="overlay" v-on:click="toggleModale('cv')"></div>
    <div class="modale card">
        <div class="btn-modale btn btn-danger" v-on:click="toggleModale('cv')">X</div>
        <slot name="cv"></slot>
    </div>
</div>

<div class="bloc-modale" v-if="reveleCdg">
    <div class="overlay" v-on:click="toggleModale('cdg')"></div>
    <div class="modale card">
        <div class="btn-modale btn btn-danger" v-on:click="toggleModale('cdg')">X</div>
        <slot name="cdg"></slot>
    </div>
</div>

<div class="bloc-modale" v-if="reveleComment">
    <div class="overlay" v-on:click="toggleModale('comment')"></div>
    <div class="modale card">
        <div class="btn-modale btn btn-danger" v-on:click="toggleModale('comment')">X</div>
        <slot name="comment"></slot>
    </div>
</div>
  </template>

<script setup>
import { defineProps } from 'vue'

defineProps({
  reveleCv: Boolean,
  reveleCdg: Boolean,
  reveleComment: Boolean,
  toggleModale: Function
})
</script>



<style scoped>

.bloc-modale{
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
    position: fixed;
}
.btn-modale{
    position: absolute;
    top: 10px;
    right: 10px;
}

</style>