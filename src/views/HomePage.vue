<template>
  <div class="container-fluid p-0">
    <div class="d-flex justify-content-start home-felirat-div">
      <h1>
        <a href="https://www.facebook.com/profile.php?id=100017469883086" class="my-name" target="_blank">Kovács János</a><span class="and"> &</span><br>
        <a href="https://www.facebook.com/profile.php?id=100010022708789" class="my-name" target="_blank">Fehér Zsolt Dorián</a><span class="and">
          &</span><br>
        <a href="https://www.facebook.com/krisztian.molnar.5437/" class="my-name" target="_blank">Molnár Krisztián</a>
      </h1>

    </div>

    <!-- <h1>HOME</h1> -->
    <img src="/public/csoportkep.png" class="img-fluid my-image" alt="csoportkep.png">
    <!-- <p class="my-clock">{{ currentTime }}</p> -->
  </div>
</template>

<script>
export default {
  data() {
    return {
      currentTime: ''
    };
  },
  mounted() {
    this.updateTime();
    setInterval(this.updateTime, 1000);
  },
  methods: {
    updateTime() {
      const now = new Date();
      this.currentTime = now.toLocaleTimeString();
    }
  }
};
</script>