<script setup>
import  CounterButton  from './components/CounterButton.vue';
import PlanPicker from './components/PlanPicker.vue';


</script>

<template>
<div class="content">
<h1 class=title>Coffe Shop</h1>
<h2 class="subtitle">The best coffee in town</h2>

<PlanPicker></PlanPicker>
</div>
</template>


<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
