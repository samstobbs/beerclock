<!-- eslint-disable vue/multi-word-component-names -->
<template>
    <h1> I drank {{ beers }} beers</h1>
    <!-- <vue3-autocounter ref='counter' :startAmount='0' :endAmount='2021' :duration='3' prefix='$' suffix='USD' separator=',' decimalSeparator='.' :decimals='2' :autoinit='true'/> -->
    <button label="Add Beer" @click="addBeer">Add Beer</button>
    <button label="Delete Beer" @click="deleteBeer">Delete Beer</button>
</template>

<script setup lang="ts">
import { ref } from 'vue';
// eslint-disable-next-line no-unused-vars
// import Vue3autocounter from 'vue3-autocounter';

const beers = ref<number>(0);
// const counter = 1000000000;
// const run = ref(true);

// while (run) {
//     addBeer();
//     // setTimeout(() => run.value = false, 20000);
// }

async function addBeer() {
    // await sleep(3000);
    beers.value = beers.value + 1;
}

function deleteBeer() {
    if (beers.value != 0){
        beers.value = beers.value - 1;
    }
}
</script>

<style>

</style>