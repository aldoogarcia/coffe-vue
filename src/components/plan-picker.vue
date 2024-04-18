<template>
    <div class="plans">
      <planPickerItem v-for="plan in plans" :name="plan" v-bind:key="plan"/>
    </div>
</template>

<script setup>
    import { ref } from 'vue';
    import planPickerItem from './plan-picker-item.vue';
    const plans=ref(["El soltero","El Adicto","El viajero","El colombiano"]);

</script>

