<script setup>
import { ref, onMounted, onBeforeUnmount } from 'vue';

const toggle = ref(false);
const dropdown = ref(null);
const katalogKnap = ref(null);
const burgermenuKnap = ref(null);

const dropdownToggle = () => {
    toggle.value = !toggle.value;
};

function clickOutside(klik) {
    if (toggle.value && !dropdown.value.contains(klik.target) && !katalogKnap.value.contains(klik.target) && !burgermenuKnap.value.contains(klik.target)) {
        toggle.value = false;
    }
    else return;
};


onMounted( () => {
    window.addEventListener("click", clickOutside);
});
onBeforeUnmount(()=> {
    window.removeEventListener("click", clickOutside);
});

</script>

<template>
    <nav>
        <div id="menu-logo">
            <router-link to="/"><img src="@/assets/dinavejling.svg" alt="Dina Vejling logo"></router-link>
        </div>

        <div id="menu-items-desktop">
            <ul id="menu-punkter">
                <li>
                    <button @click="dropdownToggle" id="katalog-knap" ref="katalogKnap">
                        Produkter<font-awesome-icon icon="fa-solid fa-angle-down" />
                    </button>
                </li>
                <li><router-link to="/arrangementer">Arrangementer</router-link></li>
                <li><router-link to="/kunstnere">Kunstnere</router-link></li>
                <li>Galleri RUMMET</li>
                <li><router-link to="/omos">Om os</router-link></li>
            </ul>
            <ul id="menu-icons">
                <li><font-awesome-icon icon="fa-solid fa-magnifying-glass" /></li>
                <li><font-awesome-icon icon="fa-solid fa-cart-shopping" /></li>
            </ul>
        </div>

        <div id="menu-items-mobile">
            <ul id="menu-icons">
                <li><font-awesome-icon icon="fa-solid fa-magnifying-glass" /></li>
                <li><font-awesome-icon icon="fa-solid fa-cart-shopping" /></li>
                <li>
                    <button @click="dropdownToggle" id="burgermenu" ref="burgermenuKnap">
                        <font-awesome-icon icon="fa-solid fa-bars" />
                    </button>
                </li>
            </ul>
        </div>

        <div id="katalog-dropdown" v-if="toggle" ref="dropdown">
            <ul class="dropdown-kategori">
                <li class="kategori-navn">Keramik og glas</li>
                <li class="kategori-link"><router-link to="/kategorier">Krus og kopper</router-link></li><hr class="divider-line">
                <li class="kategori-link">Skåle</li><hr class="divider-line">
                <li class="kategori-link">Kander</li><hr class="divider-line">
                <li class="kategori-link">Fade og tallerkener</li><hr class="divider-line">
                <li class="kategori-link">Vaser</li><hr class="divider-line">
                <li class="kategori-link">Lys og lamper</li><hr class="divider-line">
                <li class="kategori-link">Urtekopper</li><hr class="divider-line">
                <li class="kategori-link">Andre keramiske sager</li><hr class="divider-line">
            </ul>
            <ul class="dropdown-kategori">
                <li class="kategori-navn">Smykker</li><hr class="divider-line">
                <li class="kategori-link">Halskæder</li><hr class="divider-line">
                <li class="kategori-link">Øreringe</li><hr class="divider-line">
                <li class="kategori-link">Ringe</li><hr class="divider-line">
                <li class="kategori-link">Armbånd</li><hr class="divider-line">
                <li class="kategori-link">Brocher</li><hr class="divider-line">
            </ul>
            <ul class="dropdown-kategori">
                <li class="kategori-navn">Unika</li><hr class="divider-line">
                <li class="kategori-link">Vaser</li><hr class="divider-line">
                <li class="kategori-link">Skåle</li><hr class="divider-line">
                <li class="kategori-link">Badekar</li><hr class="divider-line">
                <li class="kategori-link">Objekter</li><hr class="divider-line">
                <li class="kategori-link">Fade</li><hr class="divider-line">
            </ul>
            <ul class="dropdown-kategori">
                <li class="kategori-navn">Til væggen</li><hr class="divider-line">
                <li class="kategori-link">Vægobjekter</li><hr class="divider-line">
                <li class="kategori-link">Grafik</li><hr class="divider-line">
                <li class="kategori-link">Originale tegninger</li><hr class="divider-line">
            </ul>
            <ul class="dropdown-kategori">
                <li class="kategori-navn">Diverse</li><hr class="divider-line">
                <li class="kategori-link">Snedkeri</li><hr class="divider-line">
                <li class="kategori-link">Hornvarer</li><hr class="divider-line">
                <li class="kategori-link">Tasker og punge</li><hr class="divider-line">
                <li class="kategori-link">Puder og tekstiler</li><hr class="divider-line">
                <li class="kategori-link">Jul og julepynt</li><hr class="divider-line">
                <li class="kategori-link">Flag og ranker</li><hr class="divider-line">
                <li class="kategori-link">Kort og gavekort</li><hr class="divider-line">
            </ul>
        </div>
    </nav>
    
</template>

<style>
</style>