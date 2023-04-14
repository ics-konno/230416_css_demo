<template>
    <div class="wrapper">
  <p :style="style" ref="target" class="text-shadow">{{ text }}</p>
        <textarea v-model="style" cols="40" rows="5"></textarea>
    </div>
</template>

<script lang="ts" setup>
import {ref} from "vue";

defineProps({
  text: {
    type: String,
    default: "",
  },
  color: {
    type: String,
    default: "#ff0",
  },
});

const style = ref("text-shadow: 7px 7px #ff0;");
</script>

<style scoped>
.text-shadow {
  font-weight: 700;
  font-size: 40px;
  text-shadow: 7px 7px v-bind(color);
}

.wrapper {
    display: flex;
    align-items: center;
    gap: 24px;
}

textarea {
    font-size: 24px;
}
</style>
