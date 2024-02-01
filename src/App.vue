<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
<nav class="navbar bg-dark navbar-dark">
  <div class="container">
    <router-link class="navbar-brand" to="/">
      <img src="@/assets/logo.svg" alt="Bootstrap" width="30" height="24">
      PokeAPI
    </router-link>
  </div>
  <div>
  <router-link  class="btn btn-outline-primary me-2" to="/">Home</router-link>
  <router-link class="btn btn-outline-primary me-2" to="/pokemons">Pokemons</router-link>
  <router-link class="btn btn-outline-primary " to="/favoritos">Favoritos</router-link>
</div>
</nav>
  <!-- <header>
    <img alt="Vue logo" class="logo" src="@/assets/logo.svg" width="125" height="125" />

    <div class="wrapper">
      <HelloWorld msg="You did it!" />

      <nav>
        <RouterLink to="/">Home</RouterLink>
      
        <RouterLink to="/about">About</RouterLink>
        <RouterLink to="/pokemons">Pokemons</RouterLink>
      </nav>
    </div>
  </header> -->
  <div class="container text-center"> 
  <RouterView />
</div>

  <footer>Gerardo Astorga</footer>
<div class="container text-center">
  <img src="https://easycdn.es/1/imagenes/pokemon-ultrasol-nintendo-3ds_315434_pn2.png" alt="Legendary image" width="50%">
</div>
</template>

