<script setup lang="ts">
import { ref } from "vue";
</script>

<template>
  <ul>
    <li>
      <h4 class="note-title">OpenGL Scene</h4>
      Draws a lit scene with various rotating objects. Camera can rotate with
      the mouse. The sphere is created by subdividing a tetrahedron.
    </li>
    <li>
      <h4 class="note-title">OpenMP Laplace Heatmap</h4>
      Simulates a heat distribution map with successive approximations computed
      in parallel.
    </li>
    <li>
      <h4 class="note-title">OpenMPI Mandelbrot Set</h4>
      Calculates and visualizes the Mandelbrot set in parallel with message
      passing.
    </li>
    <li>
      <h4 class="note-title">OpenMPI N-Body Orbits</h4>
      Simulates the planetary rotations of our system as an n-body problem,
      calculated in parallel with message passing. Pictured is a ten year orbit
      of the planets.
    </li>
  </ul>
</template>

<style scoped>
.img {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
</style>
