<template>
    <div class="w-full mb-20">
        <div class="w-full pt-20 pb-40 mt-10 bg-primary">
            <h3 class="text-center xs:text-3xl md:text-5xl font-bold text-white">Conheca nossas <br/>Fazendas</h3>
        </div>
        <div class="flex xs:flex-col md:flex-row xs:gap-8 md:gap-20 w-full -mt-20 xs:h-auto md:h-[350px] xs:px-4 md:px-0">
            <div class="xs:w-full md:w-[30%] shadow">
                <NuxtImg src="/farm1.png" class="object-cover w-full h-full"/>
            </div>
            <div class="xs:w-full md:w-[40%] shadow">
                <NuxtImg src="/farm2.png" class="object-cover w-full h-full"/>
            </div>
            <div class="xs:w-full md:w-[30%] shadow">
                <NuxtImg src="/farm3.png" class="object-cover w-full h-full"/>
            </div>
        </div>
    </div>

</template>

<script setup lang="ts">

</script>
