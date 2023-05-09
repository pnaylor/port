<script setup lang="ts">
import { ref } from "vue";
</script>

<template>
  <h3>WebGL Benchmark</h3>
  <li id="cell" style="padding-right: 0">
    <canvas id="canvas" width="658" height="410"></canvas>
    <br />
    <br />
    A basic benchmark exercise created to experiment with WebGL.<br />
    The JavaScript and OpenGL source is available in this page.<br />
    Can click and drag to rotate camera.<br />
  </li>
  <li id="cell" style="padding-left: 0">
    <div id="framerate" style="margin-top: 175px"></div>
    <br />
    <input type="checkbox" id="lighting" checked />
    Use Lighting
    <br />
    <input type="checkbox" id="per-pixel" checked style="display: none" />
  </li>
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
</style>
