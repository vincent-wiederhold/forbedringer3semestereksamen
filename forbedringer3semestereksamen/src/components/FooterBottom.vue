<script setup>
</script>
<template>
    <footer>
        <div class="footercontent">
            <div class="footerelements hoejre">
                <div>
                    <h4>Åbningstider</h4>
                    <ul>
                        <li>Mandag - torsdag: kl. 11.00 - 17.30</li>
                        <li>Fredag: kl. 11.00 - 18.00</li>
                        <li>Lørdag: kl. 10.30 - 14.00</li>
                        <li>Søndag: Lukket</li>
                    </ul>
                </div>
            </div>
            <div class="footerelements venstre">
                <div class="kontaktoplysninger-container">
                    <h4>Konkaktoplysinger</h4>
                    <ul>
                        <li><font-awesome-icon icon="fa-solid fa-location-dot" class="fa-lg"/> Brandtspassage 30, 5000 Odense C</li>
                        <li><font-awesome-icon icon="fa-solid fa-envelope" class="fa-lg"/> info@dinavejling.dk</li>
                        <li><font-awesome-icon icon="fa-solid fa-phone" class="fa-lg"/> +45 28 30 14 05</li>
                    </ul>
                </div>
            </div>
            <div class="footerelements hoejre">
                <div>
                    <h4>Informationer</h4>
                    <ul>
                        <li><router-link to="/omos">Om Dina Vejling</router-link></li>
                        <li>Handelsbetingelser</li>
                        <li>Galleri Rummet</li>
                        <li>Arrengementer</li>
                        <li>Kunstnere</li>
                    </ul>
                </div>
            </div>
            <div class="footerelements venstre">
                <div class="some-container">
                <h4>Følg Dina Vejling</h4>
                    <div class="some">
                        <font-awesome-icon icon="fa-brands fa-instagram" class="fa-4x"/>
                        <font-awesome-icon icon="fa-brands fa-square-facebook" class="fa-4x"/>
                    </div>
                </div>
            </div>
            <div class="footerelements venstre">
                    <div class="logo-container">
                    <img src="@/assets/dinavejling.svg" alt="" class="logo">
                </div>
            </div>
        </div>
        <div class="footerbanner">
            <p>@ 2025 Dina Vejling - Dansk Kunsthåndværk</p>
            <p>Drevet af Dina Vejling</p>
        </div>
    </footer>
</template>

<style>
</style>