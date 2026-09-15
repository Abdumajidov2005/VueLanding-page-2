<script setup>
import TheFooter from "./components/TheFooter.vue";
import TheHeader from "./components/TheHeader.vue";
import AboutSection from "./pages/AboutSection.vue";
import HeroSection from "./pages/HeroSection.vue";
import PortfolioSection from "./pages/PortfolioSection.vue";
import ServicesSection from "./pages/ServicesSection.vue";
</script>

<template>
  <div class="min-h-screen bg-[#15171d] text-white font-sans">
    <TheHeader />
    <HeroSection />
    <ServicesSection />
    <AboutSection />
    <PortfolioSection />
    <TheFooter />
  </div>
</template>
