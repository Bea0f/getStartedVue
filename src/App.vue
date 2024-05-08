<script setup lang="ts">

import Persons from './components/Persons.vue';
import Loader from './components/Loader.vue';
import Button from './components/Button.vue';
import { onMounted, ref } from 'vue';
import NumbersList from './components/NumbersList.vue';
import Pets from './components/Pets.vue';

let isLoading = ref<boolean>(true);

const removeLoader = () => {
    isLoading.value = false;
}

onMounted(() => {
    setTimeout(removeLoader, 2000);
    
})

</script>

<template>

    <Pets/>

    <NumbersList/>

    <Persons />

    <Loader v-if="isLoading" />

    <Button v-else-if="!isLoading"/>

</template>

<style scoped></style>
