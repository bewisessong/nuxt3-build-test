<template>
  <div>
    <colgroup>
      <col width="20" />
      <col width="10" />
      <col width="10" />
      <col width="10" />
      <col width="10" />
      <col width="10" />
      <col width="10" />
      <col width="10" />
      <col width="10" />
    </colgroup>

    <table>
      <tr>
        <td class="header">회의실이름1</td>
        <td></td>
        <td></td>
        <td colspan="4">요기깃</td>
        <td></td>
        <td></td>
      </tr>
      <tr>
        <td class="header">회의실이름2</td>
        <td colspan="6">요기깃</td>
        <td></td>
        <td></td>
      </tr>
    </table>
  </div>
</template>

<script setup>
const timeLine = new Array();
</script>

<style scoped>
.time {
  width: 50px;
}

table {
  border-spacing: 0px;
}
td {
  margin: 0;
  border: 1px solid brown;
}

tr:hover {
  background-color: aquamarine;
}
</style>
