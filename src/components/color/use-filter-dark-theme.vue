<template>
  <div class="bruce flex-ct-x" data-title="使用filter开启暗黑模式">
    <div class="dark-theme">
      <input type="checkbox" class="ios-switch" />
      <iframe src="https://juejin.com" class="main"></iframe>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
.btn {
  border-radius: 31px;
  width: 102px;
  height: 62px;
  background-color: #e9e9eb;
}
.dark-theme {
  display: flex;
  .ios-switch {
    position: relative;
    appearance: none;
    cursor: pointer;
    transition: all 100ms;
    @extend .btn;
    &::before {
      position: absolute;
      content: '';
      transition: all 300ms cubic-bezier(0.45, 1, 0.4, 1);
      @extend .btn;
    }
    &::after {
      position: absolute;
      left: 4px;
      top: 4px;
      border-radius: 27px;
      width: 54px;
      height: 54px;
      background-color: #fff;
      box-shadow: 1px 1px 5px rgba(#000, 0.3);
      content: '';
      transition: all 300ms cubic-bezier(0.4, 0.4, 0.25, 1.35);
    }
    &:checked {
      background-color: #5eb662;
      &::before {
        transform: scale(0);
      }
      &::after {
        transform: translateX(40px);
      }
      & + .main {
        filter: invert(1) hue-rotate(180deg);
        img,
        video,
        .avatar,
        .image,
        .thumb {
          filter: invert(1) hue-rotate(180deg);
        }
      }
    }
  }
  .main {
    margin-left: 20px;
    border: 1px solid #3c9;
    width: 1000px;
    height: 400px;
    background-color: #fff;
    transition: all 300ms;
  }
}
</style>
