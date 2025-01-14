<script setup>
import  CounterButton  from './components/CounterButton.vue';
import PlanPicker from './components/PlanPicker.vue';
import FancyButton from './components/FancyButton.vue';

import {ref} from 'vue';

const show = ref(true);


</script>

<template>
  <div class="content">
    <h1 class="title">Coffee Shop</h1>
    <h2 class="subtitle">The best coffee in town</h2>
    <FancyButton>
      <template #icon="{ hover }"> <!-- Syntax Scope Props -->
        {{ hover ? '👍' : '👌' }}
      </template>
      Submit
    </FancyButton>
    <label class="checkbox-label">
      <input class="btn-show" type="checkbox" v-model="show" />Show Plan Picker
    </label>
    <PlanPicker v-if="show"></PlanPicker>
  </div>
</template>


<style scoped>
header {
  line-height: 1.5;
}
.content {
  display: flex;
  flex-direction: column;
  align-items: center; /* Centra horizontalmente el contenido */
  justify-content: center; /* Centra verticalmente el contenido */
  height: 100vh; /* Altura completa de la ventana */
}

.checkbox-label {
  display: flex;
  align-items: center; /* Centra verticalmente el checkbox y el texto */
  cursor: pointer; /* Cambia el cursor al pasar sobre el label */
}

.btn-show {
  margin-right: 8px; /* Espacio entre el checkbox y el texto */
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
