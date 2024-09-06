<script setup>
BekertAdatok({
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
  <div class="container">
    <div class="card" style="width: 18rem">
      <img :src="`/public/${kep}.png`" class="card-img-top" :alt="`${kep}.png`" />
      <div class="card-body">
        <h5 class="card-title">{{nev}}</h5>
        <p class="card-text">
          {{bemutatkozas}}
        </p>
      </div>
    </div>
  </div>
</template>
