<template>
    <section id="hero" class="w-full xs:h-[115vh] md:h-[calc(100dvh_-_100px)] bg-cover bg-center xs:bg-[url('/bg-mobile.png')] md:bg-[url('/bg.png')]">
        <Container class="h-full flex xs:items-start md:items-center">
            <div class="flex flex-col gap-2 xs:mt-8 md:mt-0">
                <p class="xs:text-center md:text-start font-light">Chega de pagar <span class="font-bold text-primary">contas de energia abusivas</span></p>
                <h2 class="xs:text-3xl xs:text-center md:text-start md:text-5xl max-w-[500px] font-bold text-secondary">Reduza sua conta de energia em até 20% com a RS Energy</h2>

                <div class="flex flex-col xs:items-center md:items-start gap-2 mt-6">
                    <div class="flex gap-2 items-center">
                        <IconGarantia />
                        <p class="text-primary text-xl"><span class="font-bold">Garantia</span> de geracao</p>
                    </div>

                    <div class="flex gap-2 items-center">
                        <IconDesconto />
                        <p class="text-primary text-xl">Valor da sua Conta<span class="font-bold">já descontado</span></p>
                    </div>

                    <div class="flex gap-2 items-center">
                        <IconBrasil />
                        <p class="text-primary text-xl"><span class="font-bold">Empresa</span> brasileira</p>
                    </div>
                </div>

                <a href="#contato" class="mt-6 bg-primary xs:w-full md:w-[300px] py-4 flex justify-center items-center text-white font-bold rounded hover:brightness-105">EU QUERO ECONOMIZAR</a>
            </div>
        </Container>
    </section>
</template>

<script setup>

</script>
