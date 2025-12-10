<script setup>
import Arrangement from '@/components/Arrangement.vue';
import Carrusel from '@/components/Carrusel.vue';
import FooterBottom from '@/components/FooterBottom.vue';
import Navbar from '@/components/Navbar.vue';
import { ref } from "vue";

const video = ref(null);
const afspillerVideo = ref(false);

const afspilningsKnap = () => {
  // Hvis videoen er pauset, afspil den
  if (video.value.paused === true) {
    video.value.play();
  } 
  // Ellers, hvis videoen spiller, pause den
  else if (video.value.paused === false) {
    video.value.pause();
  }
};

// Videoens egens play/pause-event der opdaterer Vue statuses
const haandterPlay = () => (afspillerVideo.value = true);
const haandterPause = () => (afspillerVideo.value = false);

const aabnKort = () => {
    window.open("https://www.google.com/maps/place/Brandts+Passage+30,+5000+Odense+C", "_blank");
};
</script>


<template>
  <Navbar/>
  <figure class="herovideo">
    <!-- muted fordi video med lyd ikke må autoplayes, v-on: = @ -->
    <video
      ref="video"
      loop
      autoplay
      muted
      @play="haandterPlay"
      @pause="haandterPause"
    >
    <source src="@/assets/dinahero.mp4" />
    </video>

    <div class="hero-logo">
      <img src="@/assets/dinavejling.svg" alt="Dina Vejling logo">
    </div>

    <div class="controls">
      <button @click="afspilningsKnap">
        <font-awesome-icon v-if="afspillerVideo" icon="fa-solid fa-pause" />
        <font-awesome-icon v-else icon="fa-solid fa-play" />
      </button>
    </div>
  </figure>


  <div class="landingpagesection">
    <h1>DANSK KUNSTHÅNDVÆRK MED SJÆL</h1>
    <p>Hos Dina Vejling kan du gå på opdagelse i en verden af unikke håndplukkede værker fra over 70 professionelle kunstnere. Find os i Brandts passage i latinerkvateret i Odense.</p>
  </div>

  <div class="aabningstidersection">
    <div class="grouping">
      <h1>ÅBNINGSTIDER</h1>
      <h4>Mandag - torsdag: kl. 11.00 - 17.30</h4>
      <h4>Fredag: kl. 11.00 - 18.00</h4>
      <h4>Lørdag: 10.30 - 14.00</h4>
      <h4>Søndag: Lukket</h4>
      <div class="kontaktoplysninger">
        <p>Dina Vejling - Dansk Kunsthåndværk</p><br>
        <p>Brandts passage 30, 5000 Odense C</p>
        <p>+45 28 30 14 05</p>
      </div>
      <button @click="aabnKort"><font-awesome-icon icon="fa-solid fa-location-dot" class="fa-lg"/> FIND BUTIKKEN PÅ KORT <font-awesome-icon icon="fa-solid fa-arrow-up-right-from-square" class="arrow"/></button>
    </div>
    <img src="@/assets/dina_vejling_forside_1080x.webp" alt="">
  </div>

  <div class="dividerimage">
    <img src="@/assets/markus-winkler-JZyHRn8Cq3k-unsplash.webp" alt="">
  </div>

  <Arrangement/>
  <Carrusel/>
  <FooterBottom/>
</template>
<style scoped>
</style>