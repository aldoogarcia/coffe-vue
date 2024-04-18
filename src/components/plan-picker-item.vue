<template>
<div class="plan">
        <div class="description">
          <span class="title">
            {{ name }}
          </span>
        </div>
        <div>
          
        </div>
</div>
</template>

<script setup>
//funcion especializada integrada en vue no se importa
//defineProps(['name'])//el array va a tener una lista
//proveemos un objeto
defineProps({
  name:{
    name:String,
    type:String,
    //default:'Plan sin nombre'
    required:true
  }
})

</script>

<style lang="scss" scoped>


</style>
