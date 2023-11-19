<template>
  <footer :class="`${!hideBGCOLOR ? 'sub-bg' : ''}`">
    <div class="container">
      <div class="item md-mb50">
            <div class="title">
              <h5>Contacto</h5>
            </div>
            <ul class="flex flex-col md:flex-row justify-between">
              <li>
                <span class="icon pe-7s-map-marker"></span>
                <div class="cont">
                  <h6>Dirección</h6>
                  <p>La Unión, Murcia. Plaza Joaquín Costa nº2, 30360</p>
                </div>
              </li>
              <li>
                <span class="icon pe-7s-mail"></span>
                <div class="cont">
                  <h6>Email</h6>
                  <p>dmartindiaz3@gmail.com</p>
                </div>
              </li>
              <li>
                <span class="icon pe-7s-call"></span>
                <div class="cont">
                  <h6>Teléfono</h6>
                  <p>+34 663 56 18 97</p>
                </div>
              </li>
            </ul>
          </div>
    </div>
  </footer>
</template>

<script setup>
const { hideBGCOLOR } = defineProps(['hideBGCOLOR']);
</script>