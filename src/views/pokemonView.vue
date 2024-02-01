<script setup>
import {RouterLink} from 'vue-router'
import { useGetData } from '@/composables/getData';

const {data, getData, loading, errorData} = useGetData();
// const getData = async ( ) => {
//     try {
//       const {data} =  await axios.get('https://pokeapi.co/api/v2/pokemon/')
//         console.log(data.results);
//         pokemons.value = (data.results)
//     } catch (error) {
//         console.log(error);
        
//     }
// };
 getData("https://pokeapi.co/api/v2/pokemon/");
</script>


<template>
    <h1>Pokemons</h1>
    <p v-if="loading">Cargando informacion...</p>
    <div class="alert alert-danger mt-2" v-if="errorData"> {{ errorData }} </div>
    <div v-if="data">
    <ul class="list-group">
        <li v-for="poke in data.results" class="list-group-item">
        <router-link :to="`/pokemons/${poke.name}`">{{ poke.name }}</router-link>
    </li>
   </ul>
   <div class="mt-8">
   <button :disabled="!data.previous" class="btn btn-warning" @click="getData(data.previous)">Previus</button>
   <button :disabled="!data.next" class="btn btn-primary" @click="getData(data.next)">Next</button>
   </div>
   
</div>
</template>