<template>
  <section class="feat sub-bg section-padding">
    <div class="container">
      <div class="row">
        <div class="col-lg-8 col-md-10">
          <div class="sec-head">
            <h6 class="wow fadeIn" data-wow-delay=".5s">Sobre mi</h6>
            <h3 class="wow color-font">
              Comprometido con la creación de experiencias web.
            </h3>
            <p></p>
          </div>
        </div>
      </div>
      <div class="row">
        <div class="col-lg-3 col-md-6 items md-mb30">
          <div class="item wow fadeIn" data-wow-delay=".3s">
            <span class="icon">
              <i class="ion-ios-monitor"></i>
            </span>
            <h5>Innovador</h5>
            <p>
              Desde la implementación de nuevas funcionalidades hasta la mejora de la eficiencia del código, busco constantemente maneras de innovar y elevar el estándar en el mundo del desarrollo web.
            </p>
          </div>
        </div>
        <div class="col-lg-3 col-md-6 items active md-mb30">
          <div class="item wow fadeIn" data-wow-delay=".3s">
            <span class="icon">
              <i class="ion-ios-bolt-outline"></i>
            </span>
            <h5>Creativo</h5>
            <p>
              Mi capacidad para pensar de manera no convencional se traduce en interfaces únicas y experiencias de usuario memorables. La creatividad impulsa mi búsqueda de soluciones innovadoras y estéticamente agradables.
            </p>
          </div>
        </div>
        <div class="col-lg-3 col-md-6 items sm-mb30">
          <div class="item wow fadeIn" data-wow-delay=".3s">
            <span class="icon">
              <i class="ion-cube"></i>
            </span>
            <h5>Emprendedor</h5>
            <p>
              Mi mentalidad emprendedora me impulsa a ver cada proyecto como una oportunidad para la creación y el crecimiento. Busco constantemente nuevas formas de mejorar y superar desafíos.
            </p>
          </div>
        </div>
        <div class="col-lg-3 col-md-6 items">
          <div class="item wow fadeIn" data-wow-delay=".3s">
            <span class="icon">
              <i class="ion-ios-color-wand"></i>
            </span>
            <h5>Adaptavilidad</h5>
            <p>
              Mi capacidad para ajustarme rápidamente a nuevas tecnologías y enfoques me permite abrazar cambios y mantenerme al tanto de las últimas tendencias en el desarrollo front-end.
            </p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import cardMouseEffect from "@/common/cardMouseEffect";

onMounted(() => {
  cardMouseEffect();
});
</script>