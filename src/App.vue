<script setup lang="ts">
import { ref } from "vue";

import C from "./components/C.vue";
import Info from "./components/Info.vue";
import Godot from "./components/Godot.vue";
import Python from "./components/Python.vue";
import WebGL from "./components/WebGL.vue";

const tab = ref("");
</script>

<template>
  <div>
    <img
      src="./assets/info.svg"
      @click="tab = 'Info'"
      class="logo"
      alt="info logo"
    />
    <img src="./assets/C.svg" @click="tab = 'C'" class="logo" alt="C++ logo" />
    <img
      src="./assets/Python.svg"
      @click="tab = 'Python'"
      class="logo"
      alt="Python logo"
    />
    <img
      src="./assets/Godot.svg"
      @click="tab = 'Godot'"
      class="logo"
      alt="Godot logo"
    />
    <img
      src="./assets/WebGL.svg"
      @click="tab = 'WebGL'"
      class="logo vue"
      alt="WebGL logo"
    />
  </div>

  {{ tab }}

  <Info v-if="tab === 'Info'" msg="Vite + Vue" />
  <C v-else-if="tab === 'C'" />
  <Godot v-else-if="tab === 'Godot'" />
  <Python v-else-if="tab === 'Python'" />
  <WebGL v-else-if="tab === 'WebGL'" />

  <component :is="tab"></component>
</template>

<style scoped>
.color-red {
  list-style-position: inside;
}
.color-red ::marker {
  color: red;
}

.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
