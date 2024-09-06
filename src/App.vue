<script setup>
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'
import BemutatkozoKartya from './components/BemutatkozoKartya.vue';

</script>

<template>
<div class="container">
  <header>

      <nav>
        <RouterLink to="/">Home </RouterLink>
        <RouterLink to="/dorian">Dorián </RouterLink>
        <RouterLink to="/kiki">Kiki </RouterLink>
        <RouterLink to="/janos">János </RouterLink>
      </nav>

    </header>
  </div>


</template>