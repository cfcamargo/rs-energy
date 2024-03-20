<template>
    <transition enter-active-class="animate__animated animate__fadeInUp" leave-active-class="animate__animated animate__fadeOutDown">
        <button class="rounded-full p-4 bg-primary fixed bottom-4 right-4 border border-white shadow-md" @click="scrollToTop" v-if="showScrollButton">
            <ChevronUp color="white" />
        </button>
    </transition>
</template>

<script setup lang="ts">
import { ChevronUp } from 'lucide-vue-next'

const showScrollButton = ref(false);

const checkScroll = () => {
    if(window.scrollY > 100){
        showScrollButton.value = true;
    } else {
        showScrollButton.value = false;

    }
};

const scrollToTop = () => {
    window.scrollTo({
        top: 0,
        behavior: 'smooth'
    })
}

onMounted(() => {
    window.addEventListener('scroll', checkScroll);
});

onUnmounted(() => {
    window.removeEventListener('scroll', checkScroll);
});

</script>