<template>
  <div class="wrapper">
    <img
      :style="style"
      src="../assets/shadow-image.png"
      alt=""
      width="200"
      height="200"
    />
    <textarea v-model="style" cols="50" rows="4"></textarea>
  </div>
</template>

<script lang="ts" setup>
import { ref } from "vue";

const style = ref(
  "box-shadow: 20px 0px 50px -20px rgba(0, 0, 0, 40%), 20px 0px 50px -20px rgba(0, 0, 0, 40%) inset"
);
</script>

<style scoped>
img {
  box-shadow: 20px 0px 50px -20px rgba(0, 0, 0, 40%),
    20px 0px 50px -20px rgba(0, 0, 0, 40%) inset;
  border-radius: 50%;
}
textarea {
  font-size: 24px;
}

.wrapper {
  display: flex;
  align-items: center;
  gap: 100px;
}
</style>
