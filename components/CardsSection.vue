<template>
    <section id="results" class="py-20">
        <Container class="flex flex-col gap-10 justify-center items-center">
            <h4 class="font-bold text-5xl text-center text-secondary">Números que alavancam:</h4>
            <div class="grid xs:grid-cols-1 md:grid-cols-3 gap-8 mt-4">
                <div class="bg-primary p-8 rounded-md shadow flex flex-col gap-8">
                    <div class="flex items-center gap-4">
                        <IconMoney />
                        <span class="text-white text-3xl font-bold">+ Sustentabilidade</span>
                    </div>
                    <p class="text-justify text-white">Estamos comprometidos em liderar com soluções sustentáveis e inovadoras, atendendo às exigências ecológicas do mercado. Nosso foco é desenvolver práticas que promovam a proteção ambiental e a eficiência energética.</p>
                </div>

                <div class="bg-secondary p-8 rounded-md shadow flex flex-col gap-8">
                    <div class="flex items-center gap-4">
                        <IconPlant />
                        <span class="text-white text-3xl font-bold">+10 Toneladas</span>
                    </div>
                    <p class="text-justify text-white">Reduzimos mais de 10 toneladas de CO2 por ano com nossas soluções, demonstrando nosso compromisso ambiental. Continuaremos desenvolvendo iniciativas para um futuro mais sustentável.</p>
                </div>

                <div class="bg-primary p-8 rounded-md shadow flex flex-col gap-8">
                    <div class="flex items-center gap-4">
                        <IconTopWInner />
                        <span class="text-white text-3xl font-bold">Nossas fazenda </span>
                    </div>
                    <p class="text-justify text-white">As fazendas de energia solar estão impulsionando a economia local de forma sustentável. Utilizando tecnologias avançadas, elas reduzem a dependência de combustíveis fósseis.</p>
                </div>
            </div>
            <a href="#" class="text-center xs:w-full md:w-auto p-4 bg-primary font-bold text-2xl text-white rounded shadow brightness-105 flex justify-center gap-4 items-center">
                <span>Eu quero economizar</span>
                <IconWhatsapp />
            </a>
        </Container>
    </section>
</template>

<script setup lang="ts">

</script>