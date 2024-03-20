<template>
    <footer class="py-20 w-full bg-primary">
        <Container class="grid xs:gap-4 md:gap-20 xs:grid-cols-1 md:grid-cols-2">
            <div>
                <NuxtImg src="/logowhite.png"/>
                <div class="flex xs:flex-col md:flex-row xs:gap-10 md:gap-20 mt-10">
                    <div class="flex flex-col gap-2 text-white">
                        <span class="font-bold text-lg">Endereço</span>

                        <span>Rua Tupã, Nº637 - Ponta Porã/MS</span>
                        <span>CEP: 79901-266</span>
                    </div>
                    <div class="flex flex-col text-white">
                        <span class="font-bold text-lg">Contato</span>

                        <span>(67) 9 9871-0082</span>
                        <span>contato@sunriseenergiasolar.com.br</span>
                    </div>
                </div>
            </div>
            <div class="flex flex-col gap-8">
                <div class="flex xs:flex-col md:flex-row xs:gap-2 md:gap-10 xs:items-start md:items-center">
                    <span class="font-bold text-white text-2xl">Nossos Canais:</span>
                    <div class="flex gap-4 items-center">
                        <a href="" class="p-3 bg-zinc-800 flex justify-center items-center rounded-full">
                            <Instagram :size="30" color="white"/>
                        </a>

                        <a href="" class="p-3 bg-zinc-800 flex justify-center items-center rounded-full">
                            <Facebook :size="30" color="white"/>
                        </a>
                    </div>
                </div>
                <div>
                    <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3686.5766807139853!2d-55.72929482376878!3d-22.482536722848483!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x94626588d248181f%3A0xff9b8a28fafe1ba0!2sR.%20Tup%C3%A3%2C%20637%20-%20Jardim%20Ivone%20II%20Secao%2C%20Ponta%20Por%C3%A3%20-%20MS%2C%2079901-266!5e0!3m2!1sen!2sbr!4v1710904400340!5m2!1sen!2sbr" width="100%" height="300" style="border:0;" allowfullscreen="false" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
                </div>
            </div>
        </Container>
    </footer>
</template>

<script setup lang="ts">
import { Instagram, Facebook } from 'lucide-vue-next'
</script>

<style scoped>

</style>