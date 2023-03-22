<script setup>
import { RouterLink, RouterView } from 'vue-router'

</script>

<template>
  <nav class="navbar">
    <ul class="navbar-list">
      <li class="navbar-item"><router-link to="/">Accueil</router-link></li>
      <li class="navbar-item"><router-link to="/synopsis">Synopsis</router-link></li>
      <li class="navbar-item"><router-link to="/personnages">Personnages</router-link></li>
      <li class="navbar-item"><router-link to="/acteurs">Acteurs</router-link></li>
      <li class="navbar-item"><router-link to="/episodes">Épisodes</router-link></li>
      <li class="navbar-item"><router-link to="/anecdotes">Anecdotes</router-link></li>
      <li class="navbar-item"><router-link to="/multimedia">Multimédia</router-link></li>
      <li class="navbar-item"><router-link to="/articles-et-critiques">Articles et critiques</router-link></li>
      
      
    </ul>
  </nav>
  <RouterView></RouterView>
</template>

<script>
export default {
  name: 'Navbar'
};
</script>

<style scoped>
.navbar {
  background-color: #c0c0c0;
  padding: 10px;
  display: flex;
  justify-content: center;
}

.navbar-list {
  display: flex;
  list-style-type: none;
  padding: 0;
  margin: 0;
}

.navbar-item {
  margin: 0 5px;
}

.navbar-item a,
.router-link-exact-active,
.router-link-active {
  color: #000;
  text-decoration: none;
  font-family: 'Comic Sans MS', sans-serif;
  font-size: 14px;
  background-color: #ffcc00;
  padding: 5px 10px;
  border-radius: 5px;
  box-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
}

.navbar-item a:hover,
.router-link-exact-active:hover,
.router-link-active:hover {
  background-color: #ff9900;
  text-decoration: underline;
}
</style>
