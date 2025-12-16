<script setup>
import { computed, ref } from 'vue'; 

const kunstner = ref([]);        // kunstner-data
const startIndex = ref(0);       // start-position
const kunstnerLoaded = ref(false);

const getKunstner = async () => {
    if (kunstnerLoaded.value) return; // hent kun en gang

    try {
        const res = await fetch(
            'https://semestereksamen-85cb6-default-rtdb.europe-west1.firebasedatabase.app/kunstner.json',
            { method: 'GET' }
        );

        const response = await res.json(); // Konvertere fra JSOM til JavaScript
        kunstner.value = Object.values(response);
        kunstnerLoaded.value = true; 
    } catch (error) {
        console.error(error); // melder fejl i consollen hvis ikke det virker
    }
};

const next = () => {
    startIndex.value++; // går frem ved at lægge en til værdien
    if (startIndex.value >= kunstner.value.length) {
        startIndex.value = 0; // gør at start indexnustilles, så carusellen kan gå i loop
    }
};

// En funktion der angiver at der er 3 synlige
const synligeKunstnere = computed(() => {
    const result = [];

    for (let i = 0; i < 3; i++) { // 3 elementer
        let synligeIndex = startIndex.value + i;

        if (synligeIndex >= kunstner.value.length) {
            synligeIndex -= kunstner.value.length;
        }
        result.push(kunstner.value[synligeIndex]); // tilføjer kunstneren
    }
    return result; // viser til sammen de tre kunstnere
});


const prev = () => {
    startIndex.value--; // går tilbage ved at trække en fra værdien
    if (startIndex.value < 0) {
        startIndex.value = kunstner.value.length - 1; // trækker fra men gør at vi ikke går i minus, da den tager det element fra loopet der lige er vist
    }
};

getKunstner(); // load data
</script>

<template>
    <div class="carruselsection">
        <h1>Populære Kunstnere</h1>
        <div class="overmarging"><p>Kom ned i butikken og spørg ind til kunstnerne samt processen bag deres værker.</p></div>
        <div class="kunstnere">
            <ul v-if="kunstner.length > 0">
                <button @click="prev" aria-label="Forrige"><font-awesome-icon icon="fa-solid fa-chevron-left" class="fa-2x"/></button>
                <li v-for="kunstnerData in synligeKunstnere" :key="kunstnerData">
                    <p>{{ kunstnerData.Kunstnernavn }}</p>
                    <p>{{ kunstnerData.Profession }}</p>
                </li>
                <button @click="next" aria-label="Næste"><font-awesome-icon icon="fa-solid fa-chevron-right" class="fa-2x"/></button>
            </ul>
        </div>
    </div>
</template>
<style>
</style>