<script setup lang="ts">
import { Pet } from '../models/Pet';

const pets: Pet[] = [(new Pet("Dallas", 6, "Hund")), (new Pet("Roffe", 2, "Hund")), (new Pet("Findus", 5 , "Katt"))];

</script>

<template>
    <div id="pets-container">
        <div class="pet" v-for="(p,i) in pets">
            <h3> {{ p.name }}</h3>
            <p> {{ p.age +" år, " + p.animal }}</p>
            <p> {{ i }}</p>
        </div>
    </div>

</template>

<style scoped>
.pet {
    border: 2px blue solid;
}

</style>