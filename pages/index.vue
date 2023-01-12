<template>
  <div>
    <div>
      <button @click="moveTab('first')">first</button>
      <button @click="moveTab('second')">second</button>
    </div>
  </div>
</template>

<script setup>
const moveTab = (url) => {
  navigateTo(`/tab/${url}`);
};
</script>

<style lang="scss" scoped></style>
