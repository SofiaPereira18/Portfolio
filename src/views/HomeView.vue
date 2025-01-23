<script setup>
import myPhoto from '@/assets/selfie.jpg';

</script>

<template>
    <div class="flex justify-between space-x-4 mt-10">
        <!-- Conteudo a esquerda -->
        <div class="flex-[4] flex flex-col items-center">
            <img :src="myPhoto" alt="My photo"
            class="rounded-full"
            style="width: 300px; height: 300px;">

            <div class="text-3xl flex justify-center space-x-4 mt-5">
                <a href="https://github.com/SofiaPereira18">
                    <i class="pi pi-github hover:text-gray-500"></i>
                </a>

                <a href="https://www.linkedin.com/in/pereira-sofia/">
                    <i class="pi pi-linkedin hover:text-gray-500"></i>
                </a>
            </div>
        </div>

        <!-- Conteudo a direita -->
        <div class="flex-[6] mt-10">
            <div class="max-w-xl">
                <h1 class="text-4xl font-bold">Sofia Pereira</h1>

                <p class="mt-5 ml-2">I'm a junior front-end developer based in Lisbon, Portugal, passionate about creating intuitive and visually appealing web experiences.</p>
                <p class="ml-2">Previously, I had the opportunity to work with OutSystems, which was an exciting and unique experience that broadened my perspective on development.</p>
                <p class="ml-2">In my free time, I enjoy watching movies and TV shows.</p>
            </div>
        </div>
    </div>
</template>