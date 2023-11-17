<template>
  <div class="flex flex-row items-center fixed justify-between w-full z-50 duration-300"
    :class="{ 'bg-white': data.truescroll, 'p-1': data.truescroll, 'p-4': !data.truescroll, 'text-black': data.truescroll }">
    <p class="font-bold text-xl">Daniel Martín Díaz</p>
    <div>
      <ul class="hidden md:flex flex-row items-center">
        <li @click="jumpMenu(`inicio`)" class="m-2 p-1 hover:bg-gradient-to-tr from-pink-500 to-purple-500 hover:rounded hover:shadow-xl hover:border-b-2 duration-300">
         <Icon name = "ph:house-light"></Icon> Inicio
        </li>
        <li @click="jumpMenu(`tecnologias`)" class="m-2 p-1 hover:bg-gradient-to-tr from-pink-500 to-purple-500 hover:rounded hover:shadow-xl hover:border-b-2 duration-300">
          <Icon name = "ph:devices"></Icon> Tecnologías
        </li>
        <li @click="jumpMenu(`proyectos`)" class="m-2 p-1 hover:bg-gradient-to-tr from-pink-500 to-purple-500 hover:rounded hover:shadow-xl hover:border-b-2 duration-300">
          <Icon name = "ph:bounding-box"></Icon> Proyectos
        </li>
        <li @click="jumpMenu(`competencias`)" class="m-2 p-1 hover:bg-gradient-to-tr from-pink-500 to-purple-500 hover:rounded hover:shadow-xl hover:border-b-2 duration-300">
          <Icon name = "ph:crown-simple"></Icon> Competencias
        </li>
        <li @click="jumpMenu(`contacto`)" class="m-2 p-1 hover:bg-gradient-to-tr from-pink-500 to-purple-500 hover:rounded hover:shadow-xl hover:border-b-2 duration-300">
          <Icon name = "ph:user-circle-plus"></Icon> Contacto
        </li>
      </ul>
      <button class="md:hidden block"><Icon name="ph:list" size="1.6em"></Icon></button>
    </div>
  </div>
</template>

<script setup>
const data = reactive({
  truescroll: false
})
onMounted(() => {
  window.addEventListener('scroll', handleScroll)
})
onUnmounted(() => {
  window.removeEventListener('scroll', handleScroll);
})

const handleScroll = (e) => {
  if (window.pageYOffset > 25) {
    data.truescroll = true
  } else {
    data.truescroll = false
  }
}

const jumpMenu = (id) => {
  document.getElementById(id).scrollIntoView({behavior : "smooth"})
}
</script>

<style></style>