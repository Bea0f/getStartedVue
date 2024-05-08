<script setup lang="ts">
import { ref } from 'vue';
import { Person } from '../models/Person';

const elementId:string = "Hej";

const persons = ref<Person[]>([new Person("Beatrice", 26), new Person("Nils", 29)]);

const addPerson = () => {
    persons.value.push(new Person("Malin", 25));

}

</script>

<template>
    <div class="persons">
        <div class="person" v-for="(p,i) in persons" :key="i" >
            <h3 class="name">{{ p.name }}</h3>
            <h4 class="age" :id="elementId"> {{ p.age }}</h4>
        </div>
        
        <button @click = "addPerson"> Lägg till person</button>
    </div>
</template>

<style scoped>
.person {
    border: 2px green dotted;
    padding: 20px;
}
.name {
    color: pink;
}
.age {
    color: lightblue;
}
#Hej {
    font-size: 40px;
}
</style>
