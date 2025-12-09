<script setup>
import Navbar from '@/components/Navbar.vue';
import FooterBottom from '@/components/FooterBottom.vue';
import ImageBorder from '@/components/ImageBorder.vue';
import butikIndenfor from '@/assets/images/butik/dinavejling-butik-indenfor.jpg';
import galleriRummet from '@/assets/images/butik/galleri-rummet.jpg';

</script>

<template>
  <Navbar />
  <div class="hero about-hero">
    <h1 class="hero-text">Om os</h1>
  </div>

  <div class="section-wrapper">
    <h2 class="heading">HVEM ER VI?</h2>
    <p class="paragraf">Hos Dina Vejling sælger og udstiller vi moderne dansk kunsthåndværk af mere end 70 kunstnere. 
      Vi har alt fra keramik og glas til smykker og snedkeri, og så har vi også et mindre udvalg af 
      sølvtøj, tekstiler og grafiske kunstværker. Indehaver Dina Vejling har et bredt kendskab til 
      kunstnerne og deres værker, da hun tager ud og besøger dem på deres værksteder rundt om i landet. 
      Her bringer hun de bedste værker med hjem til Odense, så du kan gå på opdagelse i en verden af 
      ægte kunsthåndværk.</p>
    <p class="paragraf">Butikken blev etableret i 2005 og ligger i de historiske haller i den tidligere Brandts Klædefabrik. 
      Området har bevaret sit autentiske udtryk, hvilket man fornemmer i de forretninger og caféer, der 
      befinder sig her. Man fornemmer næsten den fabrikation, der fandt sted i butikslokalerne for ikke så 
      mange år siden. På den måde forbinder Dina Vejling - Dansk Kunsthåndværk sig til det historiske, 
      hvilket er noget, som vi er meget stolte af.</p>
    <div class="image-wrapper left image-border-desktop">
      <ImageBorder :src="butikIndenfor" alt="" width="700px" border="8px"/>
    </div>
    <div class="image-wrapper left image-border-mobile">
      <ImageBorder :src="butikIndenfor" alt="" width="300px" border="4px"/>
    </div>
  </div>

  <div class="section-wrapper section-dual">
    <div>
      <h2 class="heading">OVER 70 FORSKELLIGE KUNSTNERE</h2>
      <p class="paragraf">Vi samarbejder med en lang række af kunstnere over hele landet. Når Dina Vejling skal hente nye 
        værker med hjem, tager hun ud til kunstnerne på deres værksteder og ser, hvordan de arbejder. Kunstnerne er professionelt 
        uddannet enten på designskoler, kunstakademiet eller tilsvarende rundt om i landet.</p>
      <button>SE KUNSTNERE</button>
    </div>
    <div class="kunstner-quadruple">
      <img src="@/assets/images/kunstnere/akiko-og-ken.jpg" alt="Akiko og Ken">
      <img src="@/assets/images/kunstnere/anne-bannick.jpg" alt="Anne Bannick">
      <img src="@/assets/images/kunstnere/claydies.jpg" alt="Claydies">
      <img src="@/assets/images/kunstnere/jytte-kornbeck-løppenthin.jpg" alt="Jytte Kornbeck Løppenthin">
    </div>
  </div>
  
  <div>
    <div class="kontakt-section">
      <div class="kontakt-blok">
        <h2 class="width">KOM NED OG BESØG OS I BRANDTS PASSAGE!</h2>
        <p class="paragraf width">Vores butik ligger i hjertet af Odense i Latinerkvarteret ved gågaden.</p>

        <div class="adresse-blok width">
          <p class="paragraf"><font-awesome-icon icon="fa-solid fa-location-dot" class="fa-lg"/> Brandts Passage 30, 5000 Odense C</p>
        </div>

        <div class="aabningstider-blok width">
          <h3>Vores åbningstider er:</h3>
          <p class="aabningstid">Mandag - torsdag: kl. 11.00 - 17.30</p>
          <p class="aabningstid">Fredag: kl. 11.00 - 18.00</p>
          <p class="aabningstid">Lørdag: kl. 10.30 - 14.00</p>
          <p class="aabningstid">Søndag: Lukket</p>
        </div>
        
        <div class="width">
          <h3>Eller kontakt os på:</h3>
            <p class="kontakt-oplysning"><font-awesome-icon icon="fa-solid fa-envelope" /> info@dinavejling.dk</p>
            <p class="kontakt-oplysning"><font-awesome-icon icon="fa-solid fa-phone" /> +45 28 30 14 05</p>
          <button class="knap-margin"><font-awesome-icon icon="fa-solid fa-location-dot" class="fa-lg"/> FIND BUTIKKEN PÅ KORT</button>
        </div>
      </div>

      <div class="kontakt-billede">
        <img src="@/assets/images/butik/dinavejling-butik-udenfor1.webp" alt="">
      </div>
    </div>
  <div>

    </div>
  </div>

  <div class="section-wrapper section-dual">
    <div class="image-border-desktop">
      <ImageBorder :src="butikIndenfor" alt="" width="500px" border="8px"/>
    </div>
    <div class="image-border-mobile">
      <ImageBorder :src="butikIndenfor" alt="" width="200px" border="4px"/>
    </div>

    <div class="section-right">
      <h2 class="heading">ARRANGEMENTER</h2>
      <p class="paragraf">Flere gange om året afholdes der arrangementer i butikken. Det kan bl.a. være udstillinger, hvor der kommer en af vores 
        dygtige kunstnere forbi og viser deres værker frem, eller at der holdes intimkoncert eller foredrag.</p>
      <button>GÅ TIL ARRANGEMENTER</button>
    </div>
  </div>

  <div class="section-wrapper section-dual">
    <div class="section-left">
      <h2 class="heading">GALLERI RUMMET</h2>
      <p class="paragraf">I 2019 udvidede vi butikken med et galleri kaldet RUMMET for at give mere plads til udstillinger. RUMMET er med til at vise, 
        hvad kunstnerne også arbejder med. Det kan f.eks. være større installationer, gigantiske eller mikroskopiske værker eller andre projekter.</p>
      <button>SE GALLERI RUMMET</button>
    </div>
    <div class="image-border-desktop">
      <ImageBorder :src="galleriRummet" alt="" width="500px" border="8px"/>
    </div>
    <div class="image-border-mobile">
      <ImageBorder :src="galleriRummet" alt="" width="200px" border="4px"/>
    </div>
  </div>



  <FooterBottom />
</template>

<style>
</style>
