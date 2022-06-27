<template>
  <div class="bruce flex-ct-x" data-title="使用linear-gradient()描绘方格彩单">
    <div class="colour-bar"></div>
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
.colour-bar {
  width: 500px;
  height: 50px;
  background-image: repeating-linear-gradient(
    90deg,
    #f66,
    #f66 50px,
    #66f 50px,
    #66f 100px
  );
}
</style>
