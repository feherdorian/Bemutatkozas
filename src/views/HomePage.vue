<template>
  <div class="container-fluid p-0">
    <div class="d-flex justify-content-center">
      <h1 class="home-felirat">
        Kovács János & Fehér Zsolt Dorián & Molnár Krisztián
      </h1>
    </div>

    <!-- <h1>HOME</h1> -->
    <!-- <img src="/public/csoportkep.png" class="img-fluid" alt="csoportkep.png"> -->
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