<template>
  <div ref="plansWraper" class="plans">
    <plan-picker-item
      @select="printSelected"
      :selectedPlan="selectedPlan"
      v-for="plan in plans" 
      :name="plan" 
      v-bind:key="plan" />
      <p>Contador: {{ count }}</p>
  </div>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from 'vue';
import planPickerItem from './plan-picker-item.vue';
const plans = ref([
  "El soltero",
  "El adicto",
  "El viajero",]);

  const selectedPlan = ref(null);
  const plansWraper=ref(null);
  const count =ref(0);

  const printSelected = (playload) => {
    selectedPlan.value = playload;
  }
  //obteniendo la referencia del elemento utlizando queryselector
const processId =setInterval(()=>{
  console.log("incrementando")
  count.value++;
},1000)
  onMounted(() =>{
  //   const data=document.querySelector('.plans');//ayuda a tener la referencia de una element
  // console.log(data);
    console.log(plansWraper.value);
  })

  onUnmounted(() =>{
    console.log("Componente plan picker desmontado");
    clearInterval(processId);
  });
</script>
