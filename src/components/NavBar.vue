<script setup>
import NavLink from './NavLink.vue';

</script>

<template>
  <nav 
    class="bg-gray-100 border-b border-gray-300 px-6 py-4 
    flex justify-end space-x-8 pr-[200px]">

    <NavLink to="/">About</NavLink>
    <NavLink to="/experience">Experience</NavLink>
  </nav>
</template>
