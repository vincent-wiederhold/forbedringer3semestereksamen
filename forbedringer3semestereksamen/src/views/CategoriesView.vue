<script setup>
import Navbar from '@/components/Navbar.vue';
import FooterBottom from '@/components/FooterBottom.vue';
</script>

<template>
    <Navbar/>
    <div class="hero krusogkopper-hero">
    <h1 class="hero-text">Krus og kopper</h1>
  </div>
<div class="section-wrapper">
    <h2>Se udvalget af Krus og kopperne herunder</h2>
    <p>De keramiske krus og kopper er hos os speciallavet kunsthåndværk, flere forskellige slags kan ses an i butikken</p>
<div class="kategoriprodukter">
    <div class="kategoriproduktright">
        <div class="kategoriprodukt-beskrivelse">
            <div class="tekst">
                <h2>Espressokop i sort</h2>
                <p>Lavet af<b> Mia Maya</b>. Denne kop er lavet i indfarvet stentøj. Tåler opvaskemaskine og mikrobølgeovn.</p>
                <p>185 kr</p>
            </div>
        </div>
        <div class="kategoriprodukt-billede">
            <img src="@/assets/images/produkter/kopper/espresso-kop-sort-mia-maya.webp" alt="">
        </div>
    </div>
    <router-link to="/specifikprodukt">
        <div class="kategoriproduktleft">
            <div class="kategoriprodukt-beskrivelse">
                <div class="tekst">
                    <h2>Flerfarvet krus</h2>
                    <p>Lavet af<b> Clip Klap</b>. Disse Flerfarvet krus er blevet dybbet i glasur af flere omgange. Tåler opvaskemaskine</p>
                    <p>275 kr</p>
                </div>
            </div>
            <div class="kategoriprodukt-billede">
                <img src="@/assets/images/produkter/kopper/krus-stor-lyseblå-claire-maria-lehmann-og-iben-harboe.webp" alt="">
            </div>
        </div>
    </router-link>
    <div class="kategoriproduktright">
        <div class="kategoriprodukt-beskrivelse">
            <div class="tekst">
                <h2>Grå bundrillet kop</h2>
                <p>Lavet af<b> Christina Friis</b>. Denne kop er lavet i indfarvet stentøj. Tåler opvaskemaskine og mikrobølgeovn.</p>
                <p>275 kr</p>
            </div>
        </div>
        <div class="kategoriprodukt-billede">
            <img src="@/assets/images/produkter/kopper/kop-med-hank-og-riller-grå-christina-friis.webp" alt="">
        </div>
    </div>
</div>

</div>
    <FooterBottom/>
</template>

<style>
</style>