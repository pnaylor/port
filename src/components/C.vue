<script setup lang="ts">
import { ref } from "vue";
</script>

<template>
  <div>
    <h2>Computer Graphics & Computational Science Projects ~ 2011</h2>

    <table>
      <tr>
        <td>
          <img class="icon" src="../assets/C.shapes.jpeg" />
        </td>
        <td>
          <h4 class="note-title">OpenGL Scene</h4>
          Draws a lit scene with various rotating objects. Camera can rotate
          with the mouse. The sphere is created by subdividing a tetrahedron.
        </td>
      </tr>
      <tr>
        <td>
          <img class="icon" src="../assets/C.laplace.jpeg" />
        </td>
        <td>
          <h4 class="note-title">OpenMP Laplace Heatmap</h4>
          Simulates a heat distribution map with successive approximations
          computed in parallel.
        </td>
      </tr>
      <tr>
        <td>
          <img class="icon" src="../assets/C.mandel.jpeg" />
        </td>
        <td>
          <h4 class="note-title">OpenMPI Mandelbrot Set</h4>
          Calculates and visualizes the Mandelbrot set in parallel with message
          passing.
        </td>
      </tr>
      <tr>
        <td>
          <img class="icon" src="../assets/C.nbody.jpeg" />
        </td>
        <td>
          <h4 class="note-title">OpenMPI N-Body Orbits</h4>
          Simulates the planetary rotations of our system as an n-body problem,
          calculated in parallel with message passing. Pictured is a ten year
          orbit of the planets.
        </td>
      </tr>
    </table>
  </div>
</template>

<style scoped>
.icon {
  width: 8em;
  padding: 1em;
}

table {
  margin-left: auto;
  margin-right: auto;
  text-align: left;
}

td {
  vertical-align: top;
}
</style>
