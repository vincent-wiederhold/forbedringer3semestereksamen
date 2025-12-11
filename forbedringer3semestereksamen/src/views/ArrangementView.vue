<script setup>
import Arrangement from '@/components/Arrangement.vue';
import FooterBottom from '@/components/FooterBottom.vue';
import Navbar from '@/components/Navbar.vue';
</script>


<template>
  <Navbar/>
  <div class="hero arrangementer-hero">
    <h1 class="hero-text">Arrangementer</h1>
  </div>
  <div class="section-wrapper">
    <h2>Se udvalget af Krus og kopperne herunder</h2>
    <p>De keramiske krus og kopper er hos os speciallavet kunsthåndværk, flere forskellige slags kan ses an i butikken</p>
    <Arrangement/>
  </div>
  <FooterBottom/>
</template>
<style scoped>
</style>