<script setup>
import { reactive, onMounted} from 'vue';
import axios from 'axios';
import ExperienceListing from './ExperienceListing.vue';

const state = reactive({
    experience: []
});

onMounted(async () => {
    try {
        const response = await axios.get('/api/experience.json');
        state.experience = response.data.experience;
    } catch (error) {
        console.log("Erro fetching experience", error);
    }
});
</script>

<template>
   <div>
        <ExperienceListing
        v-for="exp in state.experience"
        :key="exp.id"
        :experience="exp"
        />
   </div> 
</template>