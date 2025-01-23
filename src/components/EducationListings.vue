<script setup>
import { reactive, onMounted } from 'vue';
import axios from 'axios';
import EducationListing from './EducationListing.vue';



const state = reactive({
    education: []
})

onMounted(async () => {
    try {
        const response = await axios.get('/api/education.json');
        state.education = response.data.education;
    } catch (error) {
        console.error('Error fetching educations', error);
    } 
});
</script>

<template>
    <div> 
        <EducationListing 
            v-for="edu in state.education" 
            :key="edu.id" 
            :education="edu"
        />
    </div>
</template>