<template>
    <FancyButton>
      <template v-slot:icon="slotProps">
          {{ slotProps.hoverC ? "🧨": "🐮"  }}
      </template>

      <template #default>
          <strong>E</strong>
      </template>
    </FancyButton>

    <FancyButton>
      <template #icon="{hoverC}">
        {{ hoverC ? "🧨": "🐮" }}
      </template>

      <template #default>
          <strong>E</strong>
      </template>
    </FancyButton>

  </template>
  
  <script setup>
  import FancyButton from './components/FancyButton.vue';
  </script>
  <style scoped>
 
  </style>
