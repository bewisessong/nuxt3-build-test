<template>
  <div>
    <p>First Tab Page</p>
    <input :value="firstData" />

    <br />
    <p>FirstData = {{ firstData }}</p>
  </div>
</template>

<script setup>
const firstData = ref("");
</script>
