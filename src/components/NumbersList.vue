<script setup lang="ts">
    let numbers:number[] = [1,2,3,4,5,6];
</script>

<template>
    <div id="numbers-container">
        <ul>
            <li v-for="n in numbers"> {{ n }}</li>
        </ul>
    </div>

</template>