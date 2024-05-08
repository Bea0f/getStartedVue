<script setup lang="ts">
import { ref } from "vue";

const count  = ref(0);

</script>

<template> 
<button id="myButton"  @click="count++">You clicked me {{ count }} times.</button>
<p>Detta är min knapp komponent</p>
    
</template>

<style scoped>
#myButton {
    background-color: #fff;
    color: black;
}

#myButton:hover{
    background-color: blue;
}

</style>