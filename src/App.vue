<script setup>
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'
import BemutatkozoKartya from './components/BemutatkozoKartya.vue'
</script>
 
<template>
  <header>
    <img alt="Vue logo" class="logo" src="@/assets/logo.svg" width="125" height="125" />
 
    <div class="wrapper">
      <HelloWorld msg="You did it!" />
      
      

      <nav>
        <RouterLink to="/">Home </RouterLink>
        <RouterLink to="/dorian">Dorián </RouterLink>
        <RouterLink to="/kiki">Kiki </RouterLink>
        <RouterLink to="/janos">János </RouterLink>
 
      </nav>
    </div>
  </header>
 
  <RouterView />
</template>