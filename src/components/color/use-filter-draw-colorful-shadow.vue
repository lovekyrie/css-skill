<template>
  <div class="bruce flex-ct-x" data-title="使用filter描绘彩色阴影">
    <div class="avatar-shadow"></div>
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
$avatar: 'https://feng-fortitude.com/wp-content/uploads/2022/07/thor.webp';
.avatar-shadow {
  position: relative;
  border-radius: 100%;
  width: 200px;
  height: 200px;
  background: url($avatar) no-repeat center/cover;
  &::after {
    position: absolute;
    left: 0;
    top: 10%;
    z-index: -1;
    border-radius: 100%;
    width: 100%;
    height: 100%;
    background: inherit;
    filter: blur(10px) brightness(80%) opacity(0.8);
    content: '';
    transform: scale(0.95);
  }
}
</style>
