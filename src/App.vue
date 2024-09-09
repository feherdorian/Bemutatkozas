<script setup>
import { useRouter } from 'vue-router';
import { ref } from 'vue';

// Router használata
const router = useRouter();

// Állapot létrehozása a kiválasztott elemhez
const selectedElement = ref('home');

// Navigációs és színkezelő függvények
const handleClick = (element) => {
  selectedElement.value = element; // Beállítjuk a kiválasztott elemet

  // Itt az egyes elemekhez külön navigációt adunk
  switch (element) {
    case 'home':
      router.push('/');
      break;
    case 'dorian':
      router.push('/dorian');
      break;
    case 'janos':
      router.push('/janos');
      break;
    case 'krisztian':
      router.push('/kiki');
      break;
  }
};
</script>


<template>
  <header>
    <nav class="navbar bg-body-tertiary my-navbar">
      <div class="container-fluid p-0">
        <a class="navbar-brand ps-3" href="#" data-bs-toggle="offcanvas" data-bs-target="#offcanvasExample"
          aria-controls="offcanvasExample">
          <i class="bi bi-list-nested"></i>
        </a>
      </div>
    </nav>

    <div class="container-fluid p-0">
      <RouterView />

      <div class="offcanvas offcanvas-start container-fluid p-0 list-element" tabindex="-1" id="offcanvasExample"
        aria-labelledby="offcanvasExampleLabel">

        <div class="offcanvas-header my-offcanvas-header">
          <button type="button" class="btn-close" data-bs-dismiss="offcanvas" aria-label="Close"></button>
        </div>
        <div class="offcanvas-body p-0">
          <div :class="{
            'container-fluid d-flex justify-content-center align-items-center p-5 my-element': true,
            'clicked': selectedElement === 'home'
          }" style="min-width:100%; min-height: 25%; cursor: pointer;" @click="handleClick('home')">
            <p class="home-button">HOME</p>
          </div>
          <div :class="{
            'container-fluid d-flex justify-content-center align-items-center p-5 my-element': true,
            'clicked': selectedElement === 'dorian'
          }" style="min-width:100%; min-height: 25%; cursor: pointer;" @click="handleClick('dorian')">
            <p class="">Dorián</p>
          </div>

          <div :class="{
            'container-fluid d-flex justify-content-center align-items-center p-5 my-element': true,
            'clicked': selectedElement === 'janos'
          }" style="min-width:100%; min-height: 25%; cursor: pointer;" @click="handleClick('janos')">
            <p class="">János</p>
          </div>

          <div :class="{
            'container-fluid d-flex justify-content-center align-items-center p-5 my-element': true,
            'clicked': selectedElement === 'krisztian'
          }" style="min-width:100%; min-height: 25%; cursor: pointer;" @click="handleClick('krisztian')">
            <p class="">Krisztián</p>
          </div>
        </div>
      </div>
    </div>
  </header>
</template>