<script setup>
import { RouterLink, RouterView } from 'vue-router'
import BemutatkozoKartya from './components/BemutatkozoKartya.vue'

// a másik megoldás
import { useRouter } from 'vue-router';

const router = useRouter();

const navigateHome = () => {
  router.push('/');
};
const navigateKrisztian = () => {
  router.push('/kiki');
};
const navigateJanos = () => {
  router.push('/janos');
};
const navigateDorian = () => {
  router.push('/dorian');
};

</script>

<template>
  <header>
    <!-- NAVBAR -->
    <nav class="navbar bg-body-tertiary my-navbar">
      <div class="container-fluid p-0">
        <a class="navbar-brand ps-3" href="#" data-bs-toggle="offcanvas" data-bs-target="#offcanvasExample" aria-controls="offcanvasExample">
          <i class="bi bi-list-nested"></i>
        </a>
      </div>
    </nav>


    <div class="container-fluid p-0">
      <RouterView />

      <div class="offcanvas offcanvas-start container-fluid p-0 list-element" tabindex="-1" id="offcanvasExample"
        aria-labelledby="offcanvasExampleLabel">

        <div class="offcanvas-header">
          <button type="button" class="btn-close" data-bs-dismiss="offcanvas" aria-label="Close"></button>


        </div>

        <div class="offcanvas-body p-0">
          <!-- a másik megoldás -->
          <div class="container-fliud d-flex justify-content-center p-5 my-element" @click="navigateHome"
            style="min-width:100%; min-height: 100px; cursor: pointer;">
            <p class="my-font-style home-button">
              HOME
            </p>
          </div>

          <!-- a régi megoldás -->
          <!-- <div class="container-fliud d-flex justify-content-center pt-5" onclick=""
          style=" min-width:100%; min-height: 100px;">
          <RouterLink to="/" class="text-reset text-decoration-none">Home</RouterLink>
        </div> -->


          <div class="container overflow-hidden text-center">
            <div class="row">
              <div class="gy-1">
                <div class="col-12">
                  <div class="p-3">
                    <div class="emberek-button justify-content-center p-2 my-element" 
                      @click="navigateDorian">
                      Dorián
                      <!-- regi -->
                      <!-- <RouterLink to="/dorian" class="text-reset text-decoration-none">Dorián</RouterLink> -->
                    </div>
                  </div>
                </div>
              </div>
              <div class="gy-4">
                <div class="col-12">
                  <div class="p-3">
                    <div class="emberek-button container-fliud d-flex justify-content-center p-2 my-element"
                      @click="navigateKrisztian">
                      Krisztián
                      <!-- regi -->
                      <!-- <RouterLink to="/kiki" class="text-reset text-decoration-none">Kiki</RouterLink> -->
                    </div>

                  </div>
                </div>
              </div>
              <div class="gy-4">
                <div class="col-12">
                  <div class="p-3">
                    <div class="emberek-button container-fliud d-flex justify-content-center p-2 my-element"
                      @click="navigateJanos">
                      János
                      <!-- regi -->
                      <!-- <RouterLink to="/janos" class="text-reset text-decoration-none">János</RouterLink> -->
                    </div>
                  </div>
                </div>
              </div>


            </div>
          </div>
        </div>

      </div>

    </div>
  </header>
</template>