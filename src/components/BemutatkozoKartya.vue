<script setup>
defineProps({
  nev: {
    type: String,
    required: true,
  },
  kep: {
    type: String,
    required: true,
  },
  bemutatkozas: {
    type: String,
    required: true,
  },
 
});
</script>
 
<template>
  <div class="container-fluid pt-5">
   
 
    <div class="d-flex justify-content-center">
      <div class="box">
        <div class="card" style="width: 18rem">
          <img :src="`/public/${kep}.png`" class="card-img-top" :alt="`${kep}.png`" />
          <div class="card-body">
            <h5 class="card-title">{{ nev }}</h5>
            <p class="card-text">
              {{ bemutatkozas }}
            </p>
          </div>
        </div>
      </div>
    </div>
 
  </div>
 
</template>
 
<style>
.box {
  display: inline-block;
  padding: 1rem; /* Ez a padding fogja biztosítani, hogy a border a kártya köré kerüljön */
  --border-angle: 0turn;
  --main-bg: conic-gradient(
      from var(--border-angle),
      #213,
      #112 5%,
      #112 60%,
      #213 95%
    );
 
  border: solid 5px transparent;
  border-radius: 2em;
  --gradient-border: conic-gradient(from var(--border-angle), transparent 25%, #08f, #f03 99%, transparent);
 
  background:
    var(--main-bg) padding-box,
    var(--gradient-border) border-box,
    var(--main-bg) border-box;
 
  background-position: center center;
 
  animation: bg-spin 3s linear infinite;
}
 
@keyframes bg-spin {
  to {
    --border-angle: 1turn;
  }
}
 
.box:hover {
  animation-play-state: paused;
}
 
@property --border-angle {
  syntax: "<angle>";
  inherits: true;
  initial-value: 0turn;
}
 
</style>