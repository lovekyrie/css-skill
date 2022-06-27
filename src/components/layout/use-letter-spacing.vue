<template>
  <div class="bruce flex-ct-x" data-title="使用letter-spacing排版倒序文本">
    <div class="reverse-text">恭喜发财</div>
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
.reverse-text {
  padding-left: 100px; // 与letter-spacing一致
  font-weight: bold;
  font-size: 50px;
  color: #f66;
  letter-spacing: -100px; // letter-spacing最少是font-size的两倍
}
</style>
