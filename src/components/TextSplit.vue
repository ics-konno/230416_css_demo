<template>
  <p :class="{ 'is-active': isActive }">
    <span
      v-for="(char, index) in text"
      :key="index"
      class="char"
      :style="{
        transitionDelay: `${index * 0.1}s`,
      }"
      >{{ char === " " ? "&nbsp;" : char }}</span
    >
  </p>
  <button @click="isActive = !isActive">アニメーション</button>
</template>

<script lang="ts" setup>
import { computed, ref } from "vue";

const props = defineProps({
  text: {
    type: String,
    default: "",
  },
});
const string = computed(() =>
  props.text?.split("").map((char) => {
    if (char === " ") {
      return " ";
    }
    return char;
  })
);
const isActive = ref(false);
</script>

<style scoped>
.char {
  transition: 2s opacity cubic-bezier(0.5, 0, 0, 1),
    1s transform cubic-bezier(0.5, 0, 0, 1);
  opacity: 0;
  display: inline-block;
  transform: translateX(-200%);
  font-weight: bold;
  font-size: 48px;
}
.is-active .char {
  opacity: 1;
  transform: translateX(0);
}
</style>
