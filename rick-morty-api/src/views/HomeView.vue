<script setup>
import { onMounted, reactive, ref } from 'vue';
import ListPersonagens from '../components/ListPersonagens.vue';
let personagens = reactive(ref());

onMounted(() => {
  fetch("https://rickandmortyapi.com/api/character")
  .then(response => response.json())
  .then(response => {
    personagens.value = response.results
    console.log(personagens)
  })
})

</script>

<template>
  <main class="main-container">
    <div class="container">
      <div class="row mt-4">
        <div class="col-sm-12">
          <div class="card">
            <div class="card-body row">
              <ListPersonagens 
              v-for="personagem in personagens" 
              :name="personagem.name"
              :gender="personagem.gender"
              :status="personagem.status"
              :species="personagem.species"
              :episode="personagem.episode"
              :image="personagem.image"
              :location="personagem.location.name"
            />
            </div>
          </div>
        </div>
      </div>
    </div>
  </main>   
</template>

<style>
.main-container {
  background-color: #f0f0f0;
  padding: 50px;
}

.card{
  background-color: rgb(54, 54, 55);
  color: #ffffff;
}
</style>