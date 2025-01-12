<script setup>
import CoffeePlan from './CoffeePlan.vue';
import {ref} from 'vue';

const plans = ref(['Eficent', 'Magnificent', 'Extraordinary', 'Incredible']);

const selectedCoffeePlan = ref();

function handleSelectCoffeePlan(name){
    selectedCoffeePlan.value = name;

}
</script>
<template>
<div class="plans">
    {{ selectedCoffeePlan }}
  <CoffeePlan v-for="plan in plans" 
  :key="plan" 
  :name="plan" 
  :selected="plan === selectedCoffeePlan"
  @selected="handleSelectCoffeePlan"></CoffeePlan>
</div>
</template>