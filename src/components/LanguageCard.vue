<script setup>
import { defineProps } from 'vue';

const props = defineProps({
   language: String, 
});

</script>

<template>
    <p class="inline-block px-2 py-1 bg-[#eaf2f8] rounded-lg border
     border-[#d4e6f1] text-sm">
        {{ props.language }}
    </p>

</template>