<template>
  <header class="pages-header circle-bg valign position-re">
    <div class="container">
      <div class="row justify-content-center">
        <div class="col-lg-9 col-md-11">
          <div class="capt">
            <div class="text-center">
              <h1 class="color-font mb-10 fw-700">
                {{ contentHeaderData.title.first }} <br />
                {{ contentHeaderData.title.second }}
              </h1>
              <p>{{ contentHeaderData.content }}</p>
            </div>
          </div>
        </div>
      </div>
    </div>
    <Particles id="particles-js" :options="theme === 'light' ? particlesBlackConfig : particlesConfig" />

    <div class="circle-color">
      <div class="gradient-circle"></div>
      <div class="gradient-circle two"></div>
    </div>
  </header>
</template>

<script setup>
import { ParticlesComponent as Particles } from "vue3-particles";
//= Static Data
import contentHeaderData from "@/data/contact-header.json";
import particlesConfig from "@/config/particle-config";
import particlesBlackConfig from "@/config/pr-s-black";

const { theme } = defineProps(['theme']);

onMounted(() => {
  setTimeout(() => {
    if (document.querySelector("#particles-js canvas")) {
      document.querySelector("#particles-js canvas").style.position = "unset";
    }
  }, 500);
});
</script>