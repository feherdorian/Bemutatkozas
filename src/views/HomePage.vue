<template>
  <div class="container-fluid p-0">
    <div class="row">
      <div class="col-12 text-start">
        <h1 class="home-felirat">
          <p class="fs-1">Bemutatkozás</p>
        </h1>
      </div>
      <div
        class="col-12 col-md-5 justify-content-start text-md-start mt-5 ms-5"
      >
        <h1>
          <a
            href="https://www.facebook.com/profile.php?id=100017469883086"
            class="my-name"
            target="_blank"
            >Kovács János</a
          ><span class="and"> &</span><br />
          <a
            href="https://www.facebook.com/profile.php?id=100010022708789"
            class="my-name"
            target="_blank"
            >Fehér Zsolt Dorián</a
          ><span class="and"> &</span><br />
          <a
            href="https://www.facebook.com/krisztian.molnar.5437/"
            class="my-name"
            target="_blank"
            >Molnár Krisztián</a
          >
        </h1>
        <br />
        <div class="player-container">
          <img :src="albumImage" alt="Album kép" class="album-art" />
          <audio ref="audio" :src="audioSrc" controls></audio>
          <button class="play-pause-btn p-2" @click="playPause">Play/Pause</button>
          <div class="song-list p-2">
            <button class="play-pause-btn m-2"
              v-for="song in songs"
              :key="song.id"
              @click="selectSong(song)"
            >
              {{ song.title }}
            </button>
          </div>
        </div>
        <div class="container-fluid p-0">
        </div>
      </div>
      <div class="col-12 col-md-6 text-center">
        <img
          src="/public/csoportkep.png"
          class="img-fluid my-image"
          alt="csoportkep.png"
        />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      currentTime: "",
      songs: [
        {
          id: 0,
          title: 'Kódolt Valóság v1',
          audioSrc: '/public/Kódolt Valóság v1.mp3',
          albumImage: '/public/albumcover.png',
        },
        {
          id: 1,
          title: 'Kódolt Valóság v2',
          audioSrc: '/public/Kódolt Valóság v2.mp3',
          albumImage: '/public/albumcover.png',
        },
        {
          id: 2,
          title: 'Kódolt Valóság v3',
          audioSrc: '/public/Kódolt Valóság v3.mp3',
          albumImage: '/public/albumcover.png',
        },
        {
          id: 3,
          title: 'Kódolt Valóság v4',
          audioSrc: '/public/Kódolt Valóság v4.mp3',
          albumImage: '/public/albumcover.png',
        },
      ],
      audioSrc: "/public/Kódolt Valóság v1.mp3",
      albumImage: "/public/albumcover.png",
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
    },
    playPause() {
      this.$refs.audio.paused
        ? this.$refs.audio.play()
        : this.$refs.audio.pause();
    },
    selectSong(song) {
      this.audioSrc = song.audioSrc;
      this.albumImage = song.albumImage;
      this.$refs.audio.pause(); // Pause the current song
      this.$refs.audio.load(); // Load the new song
      this.$refs.audio.play();
    },
  },
};
</script>
