<script setup>
import { computed, ref} from 'vue';

const kunstner = ref([]);
const startIndex = ref(0)
const kunstnerLoaded = ref(false)

const getKunstner = async () => {
    if (kunstnerLoaded.value) return;
    try{
        const res = await fetch('https://semestereksamen-85cb6-default-rtdb.europe-west1.firebasedatabase.app/kunstner.json',{
        method: 'GET',
        });

    const response = await res.json();

    console.log('Firebase Response', response);

    kunstner.value = Object.values(response);

    kunstnerLoaded.value = true;
 
    console.log(response)
    console.log('Kunstner Data:', kunstner.value);
    } catch(error) {
        console.error(error);
    }
};

const next = () => {
    startIndex.value++;
    if( startIndex.value >= kunstner.value.length) {
        startIndex.value = 0;
    }
};

const synligeKunstnere = computed(() => {
    const result = [];
    for (let i = 0; i< 3; i++){
        let synligeIndex = startIndex.value + i;
        if( synligeIndex >= kunstner.value.length) {
            synligeIndex = synligeIndex - kunstner.value.length;
        }
        result.push(kunstner.value[synligeIndex]);
    }
    return result;
});

const prev = () => {
    startIndex.value--;
    if (startIndex.value< 0) {
        startIndex.value = kunstner.value.length -1;
    } 
};

getKunstner();
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