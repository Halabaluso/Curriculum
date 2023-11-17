<template>
  <CommonLoading />
  <Navbar />
  <FreelanceHeader id = "inicio" />
  <Services id = "tecnologias" />
  <Works id = "proyectos" />
  <MoreServices id = "competencias" />
  <Footer id = "contacto"/>
</template>

<script setup>
//= Page components
import Navbar from '@/components/Common/NavbarDeff';
import FreelanceHeader from '@/components/Headers/FreelanceHeader';
import Services from '@/components/Services/Services5';
import MoreServices from '@/components/Services/Services3';
import Works from '@/components/Works/Works5';
import Footer from '@/components/Common/Footer';

//= Page Metadata
definePageMeta({
  layout: "dark",
});

//= Page Head
useHead({
  titleTemplate: `Daniel Martín Díaz`
});
</script>