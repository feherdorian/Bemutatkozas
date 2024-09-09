<template>

    <div class="container my-borderjani doboz">
        <h1>János</h1>

        <h1>Szia! Kovács János vagyok, aki egy közületek. Nagyon sok mindent szeretek, csak azt a zenét nem, amit a kortársaink előszeretettel hallgatnak.</h1>
        <div class="alert alert-warning" role="alert"><i class="bi bi-hearts">Nagyon félek, attól, hogy tetszik-e.</i>

        
        </div>
      
        <img :src="kep" alt="">
        <img :src="kep2" alt="">
        <h1>Ez a srác a legjobb streamer a Földön. <a href="https://twitch.tv/ave_thegamer">itt</a></h1>
    </div>


</template>

<script>
export default {
  data() {
    return {
      kep: "JanosKep1.jpg",
      kep2:"JanosKep2.jpg"
    }
  }
}
</script>

<style>

</style>