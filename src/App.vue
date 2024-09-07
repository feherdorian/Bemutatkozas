<script setup>
import { RouterLink, RouterView } from 'vue-router'
import BemutatkozoKartya from './components/BemutatkozoKartya.vue'

// a másik megoldás
import { useRouter } from 'vue-router';

const router = useRouter();

const navigateHome = () => {
  router.push('/');
};

</script>

<template>
  <header>
    <div class="container-fluid p-0">



      <button class="btn btn-primary" type="button" data-bs-toggle="offcanvas" data-bs-target="#offcanvasExample"
        aria-controls="offcanvasExample">
        <i class="bi bi-list-nested"></i>
      </button>

      <RouterView />

      <div class="offcanvas offcanvas-start container-fluid p-0" tabindex="-1" id="offcanvasExample"
        aria-labelledby="offcanvasExampleLabel">

        <div class="offcanvas-header p-0">

          <!-- a másik megoldás -->
          <div class="container-fliud d-flex justify-content-center pt-5" @click="navigateHome" style="min-width:100%; min-height: 100px; cursor: pointer;">
            HOME
          </div>

          <!-- a régi megoldás -->
          <!-- <div class="container-fliud d-flex justify-content-center pt-5" onclick=""
            style=" min-width:100%; min-height: 100px;">
            <RouterLink to="/" class="text-reset text-decoration-none">Home</RouterLink>
          </div> -->
        </div>

        <div class="offcanvas-body p-0">
          <div class="container overflow-hidden text-center">
            <div class="row">
              <div class="gy-4">
                <div class="col-12">
                  <div class="p-3">
                    <RouterLink to="/dorian" class="text-reset text-decoration-none">Dorián</RouterLink>
                  </div>
                </div>
              </div>
              <div class="gy-4">
                <div class="col-12">
                  <div class="p-3">
                    <RouterLink to="/kiki" class="text-reset text-decoration-none">Kiki</RouterLink>
                  </div>
                </div>
              </div>
              <div class="gy-4">
                <div class="col-12">
                  <div class="p-3">
                    <RouterLink to="/janos" class="text-reset text-decoration-none">János</RouterLink>
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