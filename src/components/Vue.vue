<script setup lang="ts">
import { ref } from "vue";

const focus = ref("");
</script>

<template>
  <div>
    <h2>White Label Vue LMS</h2>
    <h5>2020 ~ 2023</h5>

    <img
      src="../assets/Vue.brts.png"
      class="banner"
      alt="be ready to smile images"
    />

    <p>
      This was a project I initiated after working with Oregon Research
      Institute and Influents Innovations on their existing LMS platform for a
      few years and recognizing the limitations holding it back (see the Python
      section for more details on the legacy product). In the first year of the
      project, I lead the proposal, prototyping, and architecture phases of the
      software rebuild process. Next, my team and I completed development after
      two years of development, then launched our organization's new flagship
      product across web and mobile platforms successfully.
    </p>

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
      src="../assets/Ionic.svg"
      @click="focus = 'ionic'"
      @mouseover="focus = 'ionic'"
      @mouseleave="focus = ''"
      class="logo"
      alt="Ionic logo"
    />
    <img
      src="../assets/Firebase.svg"
      @click="focus = 'firebase'"
      @mouseover="focus = 'firebase'"
      @mouseleave="focus = ''"
      class="logo"
      alt="Firebase logo"
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
      src="../assets/Capacitor.svg"
      @click="focus = 'capacitor'"
      @mouseover="focus = 'capacitor'"
      @mouseleave="focus = ''"
      class="logo"
      alt="Capacitor logo"
    />

    <p :class="{ focused: focus === 'vue' }">Vue Framework</p>
    <p :class="{ focused: focus === 'ionic' }">Ionic Framework</p>
    <p :class="{ focused: focus === 'firebase' }">Firebase + GCP</p>
    <p :class="{ focused: focus === 'ts' }">TypeScript</p>
    <p :class="{ focused: focus === 'capacitor' }">
      Capacitor (Native Mobile Apps)
    </p>

    <h3>Major Enhancements</h3>
    <table>
      <tr>
        <th>New Software Advantages</th>
        <th>Legacy Software Limitations</th>
      </tr>
      <tr>
        <td>
          One unified codebase which compiled to native web, iOS, & Android
          versions
        </td>
        <td>
          Three different codebases, each in a different language, one for each
          distinct platform we supported
        </td>
      </tr>
      <tr>
        <td>
          A cloud based serverless backend architecture, easily scalable and
          hosted by Google Firebase
        </td>
        <td>
          Custom Django servers, hosted by our inhouse IT staff, and managed
          manually by me and our small software team
        </td>
      </tr>
      <tr>
        <td>
          Modern frontend framework and component libraries for rapid
          development and supperior visual and interactive quality
        </td>
        <td>
          No frontend framework foundation, all UI/UX design work done from
          scratch, further hindering our productivity and ability to iterate
          quickly
        </td>
      </tr>
    </table>

    <h3>Learn More</h3>
    <p>
      For a sample of hybrid mobile versions of an app compiled with the unified
      the LMS platform, please check out the
      <a href="https://apps.apple.com/us/app/beready2smile/id1668492160">
        App Store
      </a>
      and
      <a
        href="https://play.google.com/store/apps/details?id=app.web.beready2smile"
      >
        Play Store
      </a>
      pages for one of the associated project.
    </p>
    <p>
      Find more details about specific projects using the LMS platform
      <a href="https://influentsin.com/products"> here </a> in the 'Be Ready To
      Smile' & 'MomMoodBooster' product sections.
    </p>
  </div>
</template>

<style scoped>
p {
  transition: transform 0.4s;
}

table {
  max-width: 80%;
  margin-left: auto;
  margin-right: auto;
}

table,
td {
  text-align: left;
  border: 1px solid black;
}

td {
  padding: 20px;
}

.banner {
  width: 68vw;
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
