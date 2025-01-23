<script setup>
import { defineProps } from 'vue';
import LanguageCard from './LanguageCard.vue';

const props = defineProps({
    experience: Object
});

</script>


<template>
    <div class="flex justify-between space-x-4 mt-3">
        <!-- Conteúdo à esquerda -->
        <div class="flex-[7]">
            <div>
                <span class="text-xl">{{ experience.title }}</span>
                <span class="text-sm ml-2">{{ experience.company }}</span>
            </div>

            <p class="mt-2">{{ experience.location }}</p>

            <div class="flex flex-wrap gap-2 mt-4">
                <LanguageCard 
                v-for="lang in experience.languages"
                :key="lang.id"
                :language="lang"
                />
            </div>
        </div>

        <!-- Conteúdo à direita -->
        <div class="flex-[3]">
            {{ experience.duration }}
        </div>
    </div>
</template>