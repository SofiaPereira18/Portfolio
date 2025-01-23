<script setup>
import { RouterLink } from 'vue-router';

defineProps(['to']);

</script>

<template>
    <RouterLink :to="to" 
      class="text-[#2980b9] hover:text-[#2471a3] font-medium hover:shadow-md">
      
      <slot />
    </RouterLink>
  </template>