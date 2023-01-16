<template>
  <div>
    <div
      id="calendar"
      @click="clickEvent"
      style="width: 800px; height: 500px; background-color: blueviolet"
    >
      <div
        class="box-child"
        v-for="(each, index) in boxChilds"
        :key="index"
        :style="each"
      ></div>
    </div>
  </div>
</template>

<script setup>
// https://leestrument.tistory.com/entry/%ED%81%B4%EB%A6%AD%ED%95%9C-%EC%9C%84%EC%B9%98%EC%97%90-%EC%9A%94%EC%86%8C-%EC%83%9D%EC%84%B1%ED%95%98%EA%B8%B0
const boxChilds = reactive([]);

const moveTab = (url) => {
  navigateTo(`/tab/${url}`);
};

function getRandomColor() {
  const r = Math.floor(Math.random() * 100) + 100;
  const g = Math.floor(Math.random() * 100) + 100;
  const b = Math.floor(Math.random() * 100) + 100;

  return `rgb(${r}, ${g}, ${b})`;
}

const clickEvent = (e) => {
  const childSize = 20;

  console.log(e.offsetX, e.offsetY);

  const childStyle = {
    width: childSize + "px",
    height: childSize + "px",
    marginLeft: e.offsetX - childSize / 2 + "px",
    marginTop: e.offsetY - childSize / 2 + "px",
    backgroundColor: getRandomColor(),
  };

  boxChilds.push(childStyle);
};
</script>

<style scoped>
.box-child {
  box-sizing: border-box;
  position: absolute;
  background-color: red;
}

.box-child:hover {
  border: 2px solid white;
}
</style>
