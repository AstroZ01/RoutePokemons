<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>

<nav class="navbar bg-body-tertiary">
  <div class="container">
    <router-link class="navbar-brand" to="/">
      <img src="@/assets/logo.svg" alt="Bootstrap" width="30" height="24">
      PokeAPI
    </router-link>
  </div>
  <router-link  class="btn btn-outline primary" to="/">Home</router-link>
  <router-link class="btn btn-outline primary" to="/pokemons">Pokemons</router-link>
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
  <div class="container"> </div>
  <RouterView />
  <footer>Footer</footer>
</template>

