<template>
  <div class="bruce flex-ct-x" data-title="使用pointer-events禁用事件触发">
    <a href="https://www.baidu.com" class="disabled-trigger">点我</a>
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
.disabled-trigger {
  padding: 0 20px;
  border-radius: 10px;
  height: 40px;
  background-color: #66f;
  pointer-events: none;
  line-height: 40px;
  color: #fff;
}
</style>
