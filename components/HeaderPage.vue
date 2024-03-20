<template>
    <header class="bg-white h-[100px]">
        <Container class="flex justify-between items-center h-full">
            <div class="xs:w-[180px] md:w-[280px]">
                <NuxtImg src="/logo.png" class="w-full"/>
            </div>

            <nav class="flex gap-8 text-secondary" v-if="$device.isDesktop">
                <a href="#resume" class="font-semibold hover:brightness-110">Energia Solar</a>
                <a href="#farms" class="font-semibold hover:brightness-110">Fazendas</a>
                <a href="#results" class="font-semibold hover:brightness-110">Resultados</a>
                <a href="#contact" class="font-semibold hover:brightness-110">Contato</a>
            </nav>

            <a class="bg-primary text-bold px-8 py-3 rounded w-[200px] flex justify-center items-center text-white font-bold hover:brightness-105" v-if="$device.isDesktop">
                Fale Conosco
            </a>

            <button @click="toogleMenu" v-if="$device.isMobile">
                <Menu :size="40" color="#1D5E60" />
            </button>

            <transition enter-active-class="animate__animated animate__fadeInRight" leave-active-class="animate__animated animate__fadeOutRight">
                <aside class="fixed flex flex-col right-0 top-0 w-2/3 bg-primary h-dvh px-2 py-4" v-if="showMenu">
                    <div class="w-full flex justify-end">
                        <button @click="showMenu = false">
                            <X :size="30" color="white"/>
                        </button>
                    </div>
                    <nav class="flex-1 flex flex-col items-end gap-10 mt-10 text-white">
                        <a href="#resume" class="font-semibold hover:brightness-110" @click="showMenu = false">Energia Solar</a>
                        <a href="#farms" class="font-semibold hover:brightness-110" @click="showMenu = false">Fazendas</a>
                        <a href="#results" class="font-semibold hover:brightness-110" @click="showMenu = false">Resultados</a>
                        <a href="#contact" class="font-semibold hover:brightness-110" @click="showMenu = false">Contato</a>
                    </nav>

                    <a href="" class="w-full flex justify-center items-center gap-2 p-4 text-secondary bg-white rounded">
                        <span>Entrar em contato</span>
                    </a>

                </aside>
            </transition>
        </Container>
    </header>
</template>

<script setup lang="ts">
import { Menu, X } from 'lucide-vue-next'

const showMenu = ref(false)

const toogleMenu = () => {
    console.log('chamou')
    showMenu.value = !showMenu.value
}

</script>
