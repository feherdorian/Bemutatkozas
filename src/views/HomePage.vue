<template>
<div class="container-fluid p-0">
  <div class="row">
    <div class="col-12 text-start">
      <h1 class="home-felirat">
        <p class="fs-1">
          Bemutatkozás
        </p>
      </h1>
    </div>
    <div class="col-12 col-md-5 justify-content-start text-md-start mt-5 ms-5">
      <h1>
        <a href="https://www.facebook.com/profile.php?id=100017469883086" class="my-name" target="_blank">Kovács János</a><span class="and"> &</span><br>
        <a href="https://www.facebook.com/profile.php?id=100010022708789" class="my-name" target="_blank">Fehér Zsolt Dorián</a><span class="and"> &</span><br>
        <a href="https://www.facebook.com/krisztian.molnar.5437/" class="my-name" target="_blank">Molnár Krisztián</a>
      </h1>  
    </div>
    <div class="col-12 col-md-6 text-center">
      <img src="/public/csoportkep.png" class="img-fluid my-image" alt="csoportkep.png">
    </div>
  </div>
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