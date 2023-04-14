<template>
  <div class="wrapper">
    <span class="highlight" :style="style">{{ text }}</span>
    <textarea v-model="style" cols="60" rows="5"></textarea>
  </div>
</template>

<script lang="ts" setup>
import { ref } from "vue";

defineProps({
  text: {
    type: String,
    default: "",
  },
});

const style = ref("background: linear-gradient(transparent 50%, #ff0 50%);");
</script>

<style scoped>
.highlight {
  font-size: 40px;
  background: linear-gradient(transparent 50%, #ff0 50%);
}

.wrapper {
    display: flex;
    align-items: center;
    gap: 40px;
}
textarea {
    font-size: 24px;
}
</style>
