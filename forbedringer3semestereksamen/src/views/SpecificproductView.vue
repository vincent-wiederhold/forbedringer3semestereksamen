<script setup>
import FooterBottom from '@/components/FooterBottom.vue';
import Navbar from '@/components/Navbar.vue';

</script>

<template>
    <Navbar />
    <div class="breadcrumbs">
        <p><RouterLink to="/">FORSIDE</RouterLink> / <RouterLink to="/kategorier">KERAMIK OG GLAS - KRUS OG KOPPER</RouterLink> /</p>
        <p class="denne-side">FLERFARVET KRUS</p>
    </div>

    <div class="produkt-info-billeder produkt-section-wrapper hidden-on-desktop">
        <div class="produkt-info">
            <h1>Flerfarvet krus</h1>
            <p class="produkt-af">Af Clip Klap</p>
            <p class="produkt-pris">275 kr.</p>
        </div>
        <div class="produkt-stort-billede">
            <img src="@/assets/images/produkter/kopper/krus-stor-lyseblå-claire-maria-lehmann-og-iben-harboe.webp" alt="">
        </div>
        <div class="produkt-smaa-billeder">
            <img src="@/assets/images/produkter/kopper/krus-stor-lysegul-claire-maria-lehmann-og-iben-harboe.webp" alt="">
            <img src="@/assets/images/produkter/kopper/krus-stor-brun-claire-maria-lehmann-og-iben-harboe.webp" alt="">
            <img src="@/assets/images/produkter/kopper/krus-stor-lysegrøn-claire-maria-lehmann-og-iben-harboe.webp" alt="">
            <img src="@/assets/images/produkter/kopper/krus-stor-mørkegrøn-claire-maria-lehmann-og-iben-harboe.webp" alt="">
            <img src="@/assets/images/produkter/kopper/krus-stor-gul-claire-maria-lehmann-og-iben-harboe.webp" alt="">
        </div>
        <div class="produkt-tekst">
            <p>Disse flerfarvet krus er lavet af kunstnerduen Claire Maria Lehmann og Iben Harboe, der til 
                sammen hedder Clip Klap.</p>
            <p>Kruset er lavet af stentøj. For at få de forskellige farvenuancer er kruset blevet dyppet i 
                glasur af flere omgange både i dyppeglasur og reaktiv glasur. Sidenhen er rillerne blevet 
                påført, og til sidst er kruset højbrændt.</p>
            <p>Kruset kan fås i flere farver. Når kruset står i det rette lys, gengiver det et sart 
                stjernemønster på bordet. En lille hemmelig og poetisk detalje.</p>
        </div>
        <div class="produkt-knap">
            <button>LÆG I KURV</button>
        </div>
    </div>

    <div class="produkt-info-billeder produkt-section-wrapper hidden-on-mobile">
        
        <div class="produkt-dual">
            <div class="produkt-stort-billede">
                <img src="@/assets/images/produkter/kopper/krus-stor-lyseblå-claire-maria-lehmann-og-iben-harboe.webp" alt="">
            </div>
            <div class="produkt-tekst-container">
                <div class="produkt-info">
                    <h1>Flerfarvet krus</h1>
                    <p class="produkt-af">Af Clip Klap</p>
                    <p class="produkt-pris">275 kr.</p>
                </div>
                <div class="produkt-tekst">
                    <p>Disse flerfarvet krus er lavet af kunstnerduen Claire Maria Lehmann og Iben Harboe, der til 
                        sammen hedder Clip Klap.</p>
                    <p>Kruset er lavet af stentøj. For at få de forskellige farvenuancer er kruset blevet dyppet i 
                        glasur af flere omgange både i dyppeglasur og reaktiv glasur. Sidenhen er rillerne blevet 
                        påført, og til sidst er kruset højbrændt.</p>
                    <p>Kruset kan fås i flere farver. Når kruset står i det rette lys, gengiver det et sart 
                        stjernemønster på bordet. En lille hemmelig og poetisk detalje.</p>
                </div>
                <div class="produkt-knap">
                    <button>LÆG I KURV</button>
                </div>
            </div>
            
        </div>

        <div class="produkt-smaa-billeder">
            <img src="@/assets/images/produkter/kopper/krus-stor-lysegul-claire-maria-lehmann-og-iben-harboe.webp" alt="">
            <img src="@/assets/images/produkter/kopper/krus-stor-brun-claire-maria-lehmann-og-iben-harboe.webp" alt="">
            <img src="@/assets/images/produkter/kopper/krus-stor-lysegrøn-claire-maria-lehmann-og-iben-harboe.webp" alt="">
            <img src="@/assets/images/produkter/kopper/krus-stor-mørkegrøn-claire-maria-lehmann-og-iben-harboe.webp" alt="">
            <img src="@/assets/images/produkter/kopper/krus-stor-gul-claire-maria-lehmann-og-iben-harboe.webp" alt="">
        </div>
        
    </div>

    <div class="produkt-kunstner-info produkt-section-wrapper">
        <h2>Om kunstneren</h2>
        <p>Clip Klap er navnet på kunstnerduen bestående af Claire Maria Lehmann og Iben Harboe. De har arbejdet 
            sammen siden 2003, hvor de skabte deres første værk sammen, nemlig en tepotte. Clip Klap begynder 
            altid deres projekter med en definition i ord. Derved fortælles der en historie i form, materiale 
            og teknik. De kommer ind til det væsentlige og fastholder udgangspunktet i de følgende skitser. 
            De ønsker med deres keramik at videregive kunsthåndværk med liv, sanselighed og et autentisk 
            aftryk af mennesket og hånden bag.</p>
        <button>LÆS MERE OM KUNSTNEREN</button>
    </div>

    <div class="andre-produkter produkt-section-wrapper">
        <h2>Andre produkter af samme kunstner</h2>
        <div class="andre-produkter-karrusel">
            <font-awesome-icon icon="fa-solid fa-chevron-left arrows" />
            <div class="andre-produkter-billede-container">
                <img src="@/assets/images/produkter/vaser/vase-hit-the-clay-clip-klap1.webp" alt="Sort vase af keramik">
            </div>
            <div class="andre-produkter-billede-container">
                <img src="@/assets/images/produkter/tekander/tekande-clip-klap.webp" alt="Tekande">
            </div>
            <div class="andre-produkter-billede-container hidden-on-mobile">
                <img src="@/assets/images/produkter/vaser/vase-hit-the-clay-clip-klap2.webp" alt="">
            </div>
            <div class="andre-produkter-billede-container hidden-on-mobile">
                <img src="@/assets/images/produkter/vaser/vase-hit-the-clay-clip-klap3.webp" alt="">
            </div>
            <font-awesome-icon icon="fa-solid fa-chevron-right arrows" />
        </div>
    </div>


    




    <FooterBottom />
</template>

<style>
</style>