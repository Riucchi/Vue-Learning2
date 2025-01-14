<script setup>
import CoffeePlan from './CoffeePlan.vue';
import {ref, onMounted, onUnmounted} from 'vue';


const plans = ref(['Eficent', 'Magnificent', 'Extraordinary', 'Incredible']);

const selectedCoffeePlan = ref();

function handleSelectCoffeePlan(name){
    selectedCoffeePlan.value = name;
};

onMounted(() => {
  console.log(plansWrapper.value);
});

const plansWrapper = ref();


</script>
<template>
<div ref="plansWrapper" class="plans">
    {{ selectedCoffeePlan }}
  <CoffeePlan v-for="plan in plans" 
  :key="plan" 
  :name="plan" 
  :selected="plan === selectedCoffeePlan"
  @selected="handleSelectCoffeePlan"></CoffeePlan>
</div>
</template>