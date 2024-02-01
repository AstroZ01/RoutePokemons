<script setup>
import { RouterLink } from 'vue-router';
import {useFavoritosStore} from '@/store/favoritos';
import { storeToRefs } from 'pinia';
const useFavoritos = useFavoritosStore ()
const {favoritos} =  storeToRefs (useFavoritos)
const {remove} = useFavoritos;
</script>
<template>
    <h1>Favoritos</h1>
    <p v-if="favoritos.length === 0">Sin favoritos</p>
    <ul v-else class="list-group">
        <li class="list-group-item"
        v-for="poke in favoritos"
        :key="poke.id"
        >
        <div>{{ poke.name }}</div>
        <div>
            <button class="btn btn-sm btn-danger me-2" @click="remove(poke.id)">Eliminar</button>
            <router-link class="btn btn-sm btn-success" :to="`/pokemons/${poke.name}`">Mas informacion</router-link>
        </div>
    </li>
    </ul>
</template>