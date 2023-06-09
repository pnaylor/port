<script setup lang="ts">
import { ref } from "vue";

const focus = ref("");
</script>

<template>
  <div>
    <h2>C++ Graphics & Computational Science Projects</h2>
    <h5>2011</h5>

    <table>
      <tr>
        <td>
          <img
            src="../assets/C.shapes.jpeg"
            @click="focus = 'shapes'"
            @mouseover="focus = 'shapes'"
          />
        </td>
        <td class="text-cell">
          <h4 @click="focus = 'shapes'" @mouseover="focus = 'shapes'">
            OpenGL Scene
          </h4>
          <p :class="{ focused: focus === 'shapes' }">
            Draws a lit scene with various rotating objects. Camera can rotate
            with the mouse. The sphere is created by subdividing a tetrahedron.
          </p>
        </td>
      </tr>

      <tr>
        <td>
          <img
            src="../assets/C.laplace.jpeg"
            @click="focus = 'laplace'"
            @mouseover="focus = 'laplace'"
          />
        </td>
        <td class="text-cell">
          <h4 @click="focus = 'laplace'" @mouseover="focus = 'laplace'">
            OpenMP Laplace Heatmap
          </h4>
          <p :class="{ focused: focus === 'laplace' }">
            Simulates a heat distribution map with successive approximations
            computed in parallel.
          </p>
        </td>
      </tr>

      <tr>
        <td>
          <img
            src="../assets/C.mandel.jpeg"
            @click="focus = 'mandel'"
            @mouseover="focus = 'mandel'"
          />
        </td>
        <td class="text-cell">
          <h4 @click="focus = 'mandel'" @mouseover="focus = 'mandel'">
            OpenMPI Mandelbrot Set
          </h4>
          <p :class="{ focused: focus === 'mandel' }">
            Calculates and visualizes the Mandelbrot set in parallel via message
            passing.
          </p>
        </td>
      </tr>

      <tr>
        <td>
          <img
            src="../assets/C.nbody.jpeg"
            @click="focus = 'nbody'"
            @mouseover="focus = 'nbody'"
          />
        </td>
        <td class="text-cell">
          <h4 @click="focus = 'nbody'" @mouseover="focus = 'nbody'">
            OpenMPI N-Body Orbits
          </h4>
          <p :class="{ focused: focus === 'nbody' }">
            Simulates the planetary rotations of our solar system as an n-body
            problem, calculated in parallel via message passing. Visualized as a
            ten year orbit of the planets.
          </p>
        </td>
      </tr>
    </table>
  </div>
</template>

<style scoped>
img {
  border-radius: 45px;
  width: 8em;
  padding: 1em;
}

p {
  opacity: 0;
  font-size: 0.4em;
  transition: opacity 1.2s, font-size 1s;
}

table {
  margin-left: auto;
  margin-right: auto;
  text-align: left;
  max-width: 80%;
}

td {
  vertical-align: top;
}

td.text-cell {
  width: 70%;
}

.focused {
  font-size: 1em;
  opacity: 1;
  transition: opacity 2.4s, font-size 1s;
}
</style>
