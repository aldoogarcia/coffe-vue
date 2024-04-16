<template>
<div class="plan">
        <div class="description">
          <span class="title">
            {{ name }} 👍 likes {{ like }}
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
    type:String,
    //default:'Plan sin nombre'
    required:true
  },
  like:{
    type: Number,
    default:0
  }
})

</script>

<style lang="scss" scoped>


</style>
