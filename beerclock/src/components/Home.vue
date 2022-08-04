<!-- eslint-disable vue/multi-word-component-names -->
<template>
    <!-- <h1> I drank {{ beers }} beers</h1> -->
    <h1>
    <div class="flex">
        <div v-for="country in beerdata" :key="country.country">
            <div v-if="country.beer_cans_a_year != 0">
                <h2>{{ country.country }}: 
                    <Vue3autocounter ref='counter' :startAmount='0' :endAmount='country.beer_cans_a_year' :duration='31536000' separator=',' decimalSeparator='.' :autoinit='true'/>
                    <br>
                </h2>
            </div>
        </div>
    </div>
    </h1>

</template>

<script setup lang="ts">
// import { ref } from 'vue';
import Vue3autocounter from 'vue3-autocounter';
import beerdata from '../Data/beerdata.json'

</script>

<style>

</style>