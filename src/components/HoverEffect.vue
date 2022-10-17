<template>
  <div>
    <kinesis-container class="parent">
      <kinesis-element class="child" type="depth" :strength="20" />
    </kinesis-container>
  </div>
</template>

<script>
export default {
  
};
</script>

<style scoped>
.parent {
  width: 100vw;
  height: 100vh;
  position: relative;
}
.child {
  width: 100px;
  height: 100px;
  background-color: blue;
  position: absolute;
  top: calc(50vh - 50px);
  left: calc(50vw - 50px);
}
</style>
