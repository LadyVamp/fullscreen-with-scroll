<template>
  {{ msg }}
  <DemoFullscreen />
</template>

<script setup lang="ts">
import DemoFullscreen from "./DemoFullscreen.vue";

defineProps({
  msg: String,
});
</script>

<style scoped>
.read-the-docs {
  color: #888;
}
</style>
