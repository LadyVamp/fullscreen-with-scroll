<template>
  <div class="flex">
    <button @click="toggle">Go Fullscreen</button>
    <div ref="el" class="overflow-y-scroll">
      <p v-for="(n, index) in 100" :key="index">
        {{ n }}
      </p>
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref } from "vue";
import { useFullscreen } from "@vueuse/core";

const el = ref(null);
console.log(ref);

const { toggle } = useFullscreen(el);
</script>

<style scoped>
.overflow-y-scroll {
  color: orange;
  overflow-y: scroll;
}
</style>
