<template>
    <div class="content">
      
      <button v-on:mouseenter="hover=true"
              @mouseleave="hover=false">
        <slot name="icon" :hoverC="hover">⚠</slot>
        <slot>No Slot</slot>
      </button>
    </div>
  </template>
    
    <script setup>
    import {ref} from 'vue'
    const hover = ref(false);
    </script>
    <style scoped>
    .content {
      text-align: center;
    }
    .content button{
      width: 20em;
      height: 10em;
      margin: 60px auto;
      border: 2px solid black;
    }
    </style>
  