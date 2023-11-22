<template>
  <header class="freelancre valign">
    <div class="container">
      <div class="row">
        <div class="col-lg-4">
          <div class="img">
            <div class="float-area absolute">
              <div class="w-16 sm:w-20">
                <img src="../../img/vue.png" class="floating-img rounded" alt="my floating image">
              </div>
            </div>
            <div class="float-area absolute flex justify-end w-full mt-20">
              <div class="w-12 sm:w-14">
                <img src="../../img/javascript.jpg" class="floating-img rounded shadow-lg" alt="my floating image">
              </div>
            </div>
            <div class="float-area absolute flex justify-center w-full mt-44 sm:mt-64 ml-10">
              <div class="w-12 sm:w-14">
                <img src="../../img/adobexd.jpg" class="floating-img rounded shadow-lg" alt="my floating image">
              </div>
            </div>
            <div class="float-area absolute flex justify-start w-full mt-44 sm:mt-64 ml-8">
              <div class="w-12 sm:w-14">
                <img src="../../img/react.png" class="floating-img rounded shadow-lg" alt="my floating image">
              </div>
            </div>
            <img src="../../img/foto4.jpg" alt="" />
          </div>
        </div>
        <div class="col-lg-8 valign">
          <div class="cont">
            <h1 class="cd-headline clip">
              Hola, mi nombre es Daniel, apasionado de la informática y la tecnología especializado en
              <span class="cd-words-wrapper">
                <ClientOnly>
                  <AutoTyperVue :text="['JavaScript', 'Frontend', 'App web', 'Apps multiplataforma']" :repeat="Infinity"
                    initial-action="erasing" :pre-type-delay="70" :type-delay="70" :pre-erase-delay="2000"
                    :erase-delay="250" erase-style="backspace" caret-animation="smooth" class="color-font fw-600">
                  </AutoTyperVue>
                </ClientOnly>
              </span>
            </h1>
          </div>
        </div>
      </div>

      <div class="states">
        <div class="container">
          <ul class="flex">
            <li class="flex">
              <div class="numb valign">
                <h3>5</h3>
              </div>
              <div class="text valign">
                <p>
                  Años <br /> de experiencia
                </p>
              </div>
            </li>

            <li class="flex">
              <div class="numb valign">
                <h3>33</h3>
              </div>
              <div class="text valign">
                <p>
                  Proyectos completados <br /> de Frontend
                </p>
              </div>
            </li>

            <li class="mail-us">
              <a href="mailto:dmartindiaz3@gmail.com">
                <div class="flex">
                  <div class="text valign">
                    <div class="full-width">
                      <h6>dmartindiaz3@gmail.com</h6>
                      <h6>+34 663 56 18 97</h6>
                    </div>
                  </div>
                  <div class="mail-icon">
                    <div class="icon-box">
                      <span class="icon color-font pe-7s-mail"></span>
                    </div>
                  </div>
                </div>
              </a>
            </li>
          </ul>
        </div>
      </div>
    </div>
    <div class="line bottom left"></div>
  </header>
</template>

<script setup>
import { AutoTyperVue } from "auto-typer-vue3";
</script>

<style>
span.right {
  display: none !important;
}

span.caret:empty:before {
  content: "\200B";
  background: #fff;
  width: 1px;
  height: 100%;
  position: absolute;
  top: 0;
}

.floating-img {
  transform: translateY(-10%);
  animation: floater 1.5s infinite;
  transition: ease 0.5s;
  width: 70px;
  height: 70px;
}



@keyframes floater {
  0% {
    transform: translateY(-10%);
    transition: ease 0.5s;
  }

  50% {
    transform: translateY(10%);
    transition: ease 0.5s;
  }
}</style>