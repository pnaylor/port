<template>
  <transition name="fade">
    <button class="scroll-up" @click="scrollUp" v-if="isVisible">^</button>
  </transition>
</template>

<script setup lang="ts">
import { ref, onMounted, onBeforeUnmount } from "vue";

const isVisible = ref(false);

const checkVisibility = () => {
  isVisible.value = window.scrollY > 200; // Adjust the value as needed
};

const scrollUp = () => {
  window.scrollTo({ top: 0, behavior: "smooth" });
};

onMounted(() => {
  window.addEventListener("scroll", checkVisibility);
});

onBeforeUnmount(() => {
  window.removeEventListener("scroll", checkVisibility);
});
</script>

<style scoped>
.scroll-up {
  background-color: rgb(0, 188, 0);
  box-shadow: 1px 1px 4px green;
  color: black;
  font-size: large;
  height: 2em;
  position: fixed;
  bottom: 20px;
  right: 20px;
  opacity: 0.68;
}
</style>
