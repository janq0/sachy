<script setup lang="ts">
import { io } from "socket.io-client";
import { ref } from 'vue'

// const socket = io("https://server-domain.com")

const timeFormat = ref<{ initMins: number, incSecs: number } | null>(null)

const matchOpponent = () => {}
</script>

<template>
  <h2>Select the time format</h2>
  <div>
    <input type="radio" id="1+0" :value="{ initMins: 1, incSecs: 0 }" v-model="timeFormat">
    <label for="1+0">1+0</label>
    <input type="radio" id="1+1" :value="{ initMins: 1, incSecs: 1 }" v-model="timeFormat">
    <label for="1+1">1+1</label>
    <input type="radio" id="2+1" :value="{ initMins: 2, incSecs: 1 }" v-model="timeFormat">
    <label for="2+1">2+1</label>
    <input type="radio" id="3+0" :value="{ initMins: 3, incSecs: 0 }" v-model="timeFormat">
    <label for="3+0">3+0</label>
    <input type="radio" id="3+2" :value="{ initMins: 3, incSecs: 2 }" v-model="timeFormat">
    <label for="3+2">3+2</label>
    <input type="radio" id="5+0" :value="{ initMins: 5, incSecs: 0 }" v-model="timeFormat">
    <label for="5+0">5+0</label>
    <input type="radio" id="10+0" :value="{ initMins: 10, incSecs: 0 }" v-model="timeFormat">
    <label for="10+0">10+0</label>
    <input type="radio" id="15+10" :value="{ initMins: 15, incSecs: 10 }" v-model="timeFormat">
    <label for="15+10">15+10</label>
    <input type="radio" id="30+0" :value="{ initMins: 30, incSecs: 0 }" v-model="timeFormat">
    <label for="30+0">30+0</label>
  </div>
  <button @click="matchOpponent">Match an opponent</button>
</template>