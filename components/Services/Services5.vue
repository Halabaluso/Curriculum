<template>
  <section class="services box lficon section-padding position-re">
    <div class="container">
      <div class="row justify-content-center">
        <div class="col-lg-8 col-md-10">
          <div class="sec-head text-center">
            <h6 class="wow fadeIn" data-wow-delay=".5s">Tecnologías destacadas</h6>
            <h3 class="wow color-font">
              Amplia experiencia
            </h3>
          </div>
        </div>
      </div>
      <div class="row">
        <div v-for="(item, index) in featuresData" class="col-lg-6 wow fadeInLeft" :data-wow-delay="index == 0
            ? '.5s'
            : index == 1
              ? '.7s'
              : index === 2
                ? '.9s'
                : '.5s'
          " :key="item.id">
          <div class="item-box no-curve">
            <div>
              <img v-if="index === 0" src="../../img/vue.png" class="w-32">
              <img v-if="index === 1" src="../../img/nuxt.png" class="w-32">
              <img v-if="index === 2" src="../../img/react.png" class="w-32">
              <img v-if="index === 3" src="../../img/github.png" class="w-28">
              <img v-if="index === 4" src="../../img/firebase.png" class="w-28">
              <img v-if="index === 5" src="../../img/adobexd.jpg" class="w-28">
            </div>
            <div class="cont">
              <h6>{{ item.title }}</h6>
              <p>{{ item.content }}</p>
              <p class="mt-1 italic text-white">{{ item.subcontent }}</p>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="line bottom right"></div>
  </section>
</template>

<script setup>
import featuresData from "@/data/features.json";
</script>