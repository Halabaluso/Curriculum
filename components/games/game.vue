<template>
    <div class="flex flex-col items-center justify-center portfolio-frl section-padding pb-70">
        <div class="container mt-10">
      <div class="row justify-content-center">
        <div class="col-lg-8 col-md-10">
          <div class="sec-head text-center">
            <h6 class="wow fadeIn" data-wow-delay=".5s">Enfréntate a mi IA 🤖</h6>
            <h3 class="wow color-font">
              ¿Jugamos?
            </h3>
          </div>
        </div>
      </div>
    </div>
        <div class="grid grid-cols-2 gap-5">
            <div class="min-w-72 max-w-xs">
                <p class="text-center text-green-400 text-2xl font-bold">🤓 Tú {{ data.favourcount }}</p>
                <img v-if="data.enemy === 0" src="../../img/paper2.png" alt="">
                <img v-if="data.enemy === 1" src="../../img/cut2.png" alt="">
                <img v-if="data.enemy === 2" src="../../img/rock2.png" alt="">
            </div>
            <div class="min-w-72 max-w-xs">
                <p class="text-center text-2xl font-bold text-red-400">🤖 IA {{ data.enemycount }}</p>
                <img v-if="data.favour === 0" src="../../img/paper1.png" alt="">
                <img v-if="data.favour === 1" src="../../img/cut1.png" alt="">
                <img v-if="data.favour === 2" src="../../img/rock1.png" alt="">
            </div>
        </div>
        <div class="text-center">
                <p :class=data.dinamicClassWin >Tú ganas. 🙁</p>
                <p :class=data.dinamicClassLose >Yo gano. 🤩</p>
            <button id = "butongame" @click="playGame"
                class="bg-gradient-to-tr from-purple-500 to-pink-500 p-2 w-52 text-lg rounded-full text-black duration-300 hover:-translate-y-2 hover:font-bold">Jugar</button>
        </div>
    </div>
</template>
<script lang="ts" setup>
import { customAlphabet } from 'nanoid'
interface ReactiveInterface {
    enemyarray: Array<number>,
    favourarray: Array<number>,
    enemy: number,
    favour: number,
    enemycount: number,
    favourcount: number,
    dinamicClassWin: string,
    dinamicClassLose: string
}
const data = reactive<ReactiveInterface>({
    //0 paper 1 tijera 2 piedra
    enemyarray: [0, 1, 2],
    favourarray: [0, 1, 2],
    enemy: 0,
    favour: 0,
    enemycount: 0,
    favourcount: 0,
    dinamicClassWin: "hidden duration-300",
    dinamicClassLose: "hidden duration-300",
})

const playGame = () => {
    const buttom: any = document.getElementById("butongame")
    buttom.disabled = true
    clearInterval(interval)
    setTimeout(() => {
        interval = setInterval(GameFunction, 300)
        data.dinamicClassLose = "hidden duration-300"
        data.dinamicClassWin = "hidden duration-300"
        buttom.disabled = false
    }, 2000)
    switch (data.enemy) {
        case 0:
            console.log("Pasa1")
            if (data.favour == 0) {
                data.enemycount = data.enemycount + 1
                data.favourcount = data.favourcount + 1
            }
            if (data.favour == 1) {
                data.dinamicClassWin = "my-5 text-xl font-bold text-green-400 duration-300"
                data.favourcount = data.favourcount + 1
            }
            if (data.favour == 2) {
                data.dinamicClassLose = "my-5 text-xl font-bold text-red-400 duration-300"
                data.enemycount = data.enemycount + 1
            }
            break;
        case 1: 
            if (data.favour == 0) {
                data.dinamicClassWin = "my-5 text-xl font-bold text-green-400 duration-300"
                data.favourcount = data.favourcount + 1
            }
            if (data.favour == 1) {
                data.enemycount = data.enemycount + 1
                data.favourcount = data.favourcount + 1
            }
            if (data.favour == 2) {
                data.dinamicClassLose = "my-5 text-xl font-bold text-red-400 duration-300"
                data.enemycount = data.enemycount + 1
            }
            break;
        case 2:
            if (data.favour == 0) {
                data.dinamicClassLose = "my-5 text-xl font-bold text-red-400 duration-300"
                data.enemycount = data.enemycount + 1
            }
            if (data.favour == 1) {
                data.dinamicClassWin = "my-5 text-xl font-bold text-green-400 duration-300"
                data.favourcount = data.favourcount + 1
            }
            if (data.favour == 2) {
                data.enemycount = data.enemycount + 1
                data.favourcount = data.favourcount + 1
            }
            break;

        default:
            break;
    }
}

const nanoid = customAlphabet('012', 1)
const GameFunction = () => {
    const ramdomId = nanoid()
    data.enemy = data.enemyarray[parseInt(ramdomId)]
    const ramdomId2 = nanoid()
    data.favour = data.favourarray[parseInt(ramdomId2)]
}

let interval = setInterval(GameFunction, 300)
</script>