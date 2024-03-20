<template>
    <Swiper
        :modules="[SwiperAutoplay, SwiperEffectCreative, SwiperNavigation]"
        :slides-per-view="slidesPerView"
        :loop="true"
        :navigation="true"
        :autoplay="{
            delay: 8000,
            disableOnInteraction: true,
        }"
        >
        <SwiperSlide v-for="slide in 10" :key="slide" class="px-2">
            <div class="w-full h-[400px] bg-gray-200 flex justify-center items-center">
                texto do cliente
            </div>
        </SwiperSlide>
    </Swiper>
</template>

<script setup lang="ts">
const { isMobile } = useDevice();

const slidesPerView = computed(() => {
    if (isMobile) {
        return 1;
    }
    return 2;
})

</script>
