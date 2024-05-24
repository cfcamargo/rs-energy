<template>
  <HeaderPage />
  <main>
    <HeroSection />
    <ResumeSection />
    <FarmsSection />
    <CardsSection />
    <!-- <Testimonials /> -->
    <CallToActionBanner />
    <!-- <EmployerSection /> -->
    <Contact />
  </main>
  <FooterSection />
  <OwnerFooter />
  <ScrollToTop />
</template>

<script>
import 'animate.css';
import OwnerFooter from './components/OwnerFooter.vue';

useHead({
  title: 'RS Energy | Soluções em Energia Solar',
  meta: [
    { name: 'description', content: 'Para residências, empresas e propriedades rurais com contas de luz superiores a R$ 500,00 por mês, com um consumo mínimo de 600 kWh, apresentamos uma solução vantajosa. Com a nossa Assinatura Solar, todos saem ganhando: você economiza, seu negócio prospera e o meio ambiente se beneficia. Descubra como reduzir seus gastos com energia elétrica sem nenhum investimento inicial.' }
  ],
})

</script>
