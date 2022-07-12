<template>
  <div class="bruce flex-ct-x" data-title="使用box-shadow裁剪聚焦区域">
    <div class="img-cliper">
      <img src="https://feng-fortitude.com/wp-content/uploads/2022/07/gz.jpg" alt="" />
      <i> </i>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
.img-cliper {
  overflow: hidden;
  position: relative;
  img {
    width: 400px;
  }
  i {
    position: absolute;
    left: 50px;
    top: 30px;
    border-radius: 100%;
    width: 100px;
    height: 50px;
    box-shadow: 0 0 0 9999px rgba(#000, 0.5);
  }
}
</style>
