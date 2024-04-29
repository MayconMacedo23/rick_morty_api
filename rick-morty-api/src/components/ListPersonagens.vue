<script setup>
const personagem = defineProps(["name","gender","status","species","episode","image","location"])
</script>

<template>
    <div class="col-md-4">
        <div class="card p-2 mb-3">
            <img :src="personagem.image" style="border-radius: 5%;"> </img>
            <p class="text-center">Nome: {{ personagem.name }}</p>
            <p class="text-center">Gênero: {{ personagem.gender }}</p>
            <p class="text-center">Status: {{ personagem.status }}</p>
            <p class="text-center">Espécie: {{ personagem.species }}</p>
            <p class="text-center">Episódios: {{ personagem.episode.length }}</p>
            <p class="text-center">Localização: {{ personagem.location }}</p>

        </div>
    </div>
</template>

<style>

</style>