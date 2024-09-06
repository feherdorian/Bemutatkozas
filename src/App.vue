<script setup>
import { RouterLink, RouterView } from 'vue-router'
import BemutatkozoKartya from './components/BemutatkozoKartya.vue'

</script>

<template>
  <header>
    <div class="container-fluid p-0">
      <nav class="navbar navbar-expand-lg bg-body-tertiary">
        <div class="container-fluid">
          <a class="navbar-brand" href="#"><RouterLink to="/" class="text-reset text-decoration-none">Home</RouterLink></a>
          <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav"
            aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
            <span class="navbar-toggler-icon"></span>
          </button>
          <div class="collapse navbar-collapse" id="navbarNav">
            <ul class="navbar-nav">
              <li class="nav-item">
                <a class="nav-link" href="#"><RouterLink to="/dorian" class="text-reset text-decoration-none">Dorián</RouterLink></a>
              </li>
              <li class="nav-item">
                <a class="nav-link" href="#"><RouterLink to="/kiki" class="text-reset text-decoration-none">Kiki</RouterLink></a>
              </li>
              <li class="nav-item">
                <a class="nav-link" href="#"><RouterLink to="/janos" class="text-reset text-decoration-none">János</RouterLink></a>
              </li>
            </ul>
          </div>
        </div>
      </nav>

      <RouterView />
    </div>
  </header>
</template>