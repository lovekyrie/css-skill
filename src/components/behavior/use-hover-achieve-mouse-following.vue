<template>
  <div class="bruce flex-ct-x" data-title="使用:hover描绘鼠标跟随">
    <ul class="mouse-following">
      <li v-for="v in 500" :key="v"></li>
    </ul>
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
@function random-num($max, $min: 0, $u: 1) {
  @return ($min + random($max)) * $u;
}
.bruce {
  padding: 0;
}
.mouse-following {
  display: flex;
  overflow: hidden;
  flex-wrap: wrap;
  height: 100%;
  cursor: pointer;
  li {
    position: relative;
    width: 30px;
    height: 30px;
    &::before {
      position: absolute;
      left: 0;
      right: 0;
      top: 0;
      bottom: 0;
      border-radius: 100%;
      background-color: transparent;
      content: '';
      transform: scale3d(0.1, 0.1, 0.1);
      transition: all 500ms ease-in;
    }
    &:hover {
      &::before {
        transform: translate3d(1.8, 1.8, 1.8);
        transition: transform 0s;
      }
    }
    @for $i from 1 through 500 {
      &:nth-child(#{$i}):hover {
        &::before {
          background-color: rgba(
            random-num(255),
            random-num(255),
            random-num(255),
            0.8
          );
        }
      }
    }
  }
}
</style>
