<script setup lang="ts">
import { ref } from "vue";

import C from "./components/C.vue";
import Info from "./components/Info.vue";
import Godot from "./components/Godot.vue";
import Python from "./components/Python.vue";
import Vue from "./components/Vue.vue";
import WebGL from "./components/WebGL.vue";

const tab = ref("");
</script>

<template>
  <div>
    <img
      src="./assets/Vue.svg"
      @click="tab = 'Vue'"
      class="logo"
      :class="{ active: tab === 'Vue' }"
      alt="Vue logo"
    />
    <img
      src="./assets/Python.svg"
      @click="tab = 'Python'"
      class="logo"
      :class="{ active: tab === 'Python' }"
      alt="Python logo"
    />
    <img
      src="./assets/C.svg"
      @click="tab = 'C'"
      class="logo"
      :class="{ active: tab === 'C' }"
      alt="C++ logo"
    />
    <!-- 
    <img
      src="./assets/Godot.svg"
      @click="tab = 'Godot'"
      class="logo"
      :class="{ active: tab === 'Godot' }"
      alt="Godot logo"
    />
    <img
      src="./assets/WebGL.svg"
      @click="tab = 'WebGL'"
      class="logo"
      alt="WebGL logo"
    />
    -->
    <img
      src="./assets/info.svg"
      @click="tab = 'Info'"
      class="logo"
      :class="{ active: tab === 'Info' }"
      alt="info logo"
    />
  </div>

  <Transition name="fade" mode="out-in">
    <C v-if="tab === 'C'" />
    <Godot v-else-if="tab === 'Godot'" />
    <Python v-else-if="tab === 'Python'" />
    <Vue v-else-if="tab === 'Vue'" />
    <WebGL v-else-if="tab === 'WebGL'" />
    <Info v-else-if="tab === 'Info'" />
  </Transition>

  <component :is="tab"></component>

  <footer>
    Paul Naylor
    <br />
    Made with
    <img src="./assets/Vue.svg" class="icon" alt="Vue logo" />ue
  </footer>
</template>

<style scoped>
footer {
  /* position: fixed; */
  margin-top: 48%;
}
.active {
  filter: drop-shadow(0 0 1em green);
}

.fade-enter-active,
.fade-leave-active {
  transition: all 0.4s ease;
}

.fade-enter-from {
  opacity: 0;
  transform: translateY(-10px);
}

.fade-leave-to {
  opacity: 0;
  transform: translateY(10px);
}

.icon {
  height: 0.88em;
}

.logo {
  height: 6em;
  margin: 2.4em;
  will-change: filter;
  transition: transform 0.4s, filter 0.4s ease-out;
}

.logo:hover {
  filter: drop-shadow(0 0 1.2em blue);
}

@media only screen and (max-width: 600px) {
  .logo {
    height: 4em;
    margin: 1.2em;
  }
}
</style>
