<template>
<div @click="selec()"
    :class="{'selected-plan' : selected}" class="plan">
        <div class="description">
          <span class="title">
            {{ name }}{{ selected ? " ✅":"" }}
          </span>
        </div>
        <div>
          
        </div>
</div>
</template>

<script setup>
import { ref } from 'vue';

//funcion especializada integrada en vue no se importa
//defineProps(['name'])//el array va a tener una lista
//proveemos un objeto
const selected=ref(false);
const selec = ()=>{
  selected.value=true;
}
defineProps({
  name:{
    name:String,
    type:String,
    //default:'Plan sin nombre'
    required:true
  }
})

</script>

<style scoped>
.selected-plan{
  border:3px solid red;

}


</style>
