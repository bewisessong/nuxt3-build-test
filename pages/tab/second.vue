<template>
  <div>
    <p>Second Tab Page</p>
    <input :value="secondData" />

    <br />
    <p>SecondData = {{ secondData }}</p>
  </div>
</template>

<script setup>
const secondData = ref("");
</script>
