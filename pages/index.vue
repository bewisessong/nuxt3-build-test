<template>
  <div>
    <div>
      <button @click="moveTab('first')">first</button>
      <button @click="moveTab('second')">second</button>
    </div>

    <timeline />
  </div>
</template>

<script setup>
import timeline from "@/pages/timeline";

const moveTab = (url) => {
  navigateTo(`/tab/${url}`);
};
</script>

<style lang="scss" scoped></style>
