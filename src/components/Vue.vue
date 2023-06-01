<script setup lang="ts">
import { ref } from "vue";

const focus = ref("");
</script>

<template>
  <div>
    <h2>White Label Vue LMS</h2>
    <h5>2020 ~ 2023</h5>
    <p>
      This was a project I initiated after working with Oregon Research
      Institute and Influents Innovations on their existing LMS platform for a
      couple years, and recognizing the need to modernize it (see the Python
      section for more details on that previous project). I lead the proposal,
      prototyping, and architecture processes for the new iteration of the
      application, and my team completed development of the new flagship product
      for our organization over a three year process.
    </p>

    <div class="fit">
      <img src="../assets/Vue.brts.png" />
    </div>

    <h3>Tech Stack</h3>
    <img
      src="../assets/Vue.svg"
      @click="focus = 'vue'"
      @mouseover="focus = 'vue'"
      @mouseleave="focus = ''"
      class="logo"
      alt="Vue logo"
    />
    <img
      src="../assets/TS.svg"
      @click="focus = 'ts'"
      @mouseover="focus = 'ts'"
      @mouseleave="focus = ''"
      class="logo"
      alt="TypeScript logo"
    />
    <img
      src="../assets/Ionic.svg"
      @click="focus = 'ionic'"
      @mouseover="focus = 'ionic'"
      @mouseleave="focus = ''"
      class="logo"
      alt="Ionic logo"
    />
    <img
      src="../assets/Capacitor.svg"
      @click="focus = 'capacitor'"
      @mouseover="focus = 'capacitor'"
      @mouseleave="focus = ''"
      class="logo"
      alt="Capacitor logo"
    />
    <img
      src="../assets/Firebase.svg"
      @click="focus = 'firebase'"
      @mouseover="focus = 'firebase'"
      @mouseleave="focus = ''"
      class="logo"
      alt="Firebase logo"
    />

    <p :class="{ focused: focus === 'vue' }">Vue 3</p>
    <p :class="{ focused: focus === 'ts' }">TypeScript</p>
    <p :class="{ focused: focus === 'ionic' }">Ionic Framework</p>
    <p :class="{ focused: focus === 'capacitor' }">
      Capacitor (Native Mobile Apps)
    </p>
    <p :class="{ focused: focus === 'firebase' }">Firebase / GCP</p>

    <h3>Learn More</h3>
    <p>
      Find more details <a href="https://influentsin.com/products"> here </a>
      in the 'Be Ready To Smile' & 'MomMoodBooster' product sections.
    </p>
  </div>
</template>

<style scoped>
div.fit {
  width: 80vw;
  margin: auto;
  display: block;
}

img {
  max-width: 100%;
  height: auto;
}

p {
  transition: transform 0.4s;
}

.focused {
  transform: scale(1.8);
}

.logo {
  height: 4em;
  padding: 1em;
}

.logo:hover {
  transform: scale(1.4);
}
</style>
