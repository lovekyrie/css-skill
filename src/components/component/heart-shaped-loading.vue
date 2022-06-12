<template>
  <div class="bruce flex-ct-x" data-title="心形加载条">
    <div class="heart-loading">
      <ul style="--line-count: 9">
        <li
          v-for="v in 9"
          :key="v"
          :class="`line-${v}`"
          :style="`--line-index: ${v}`"
        ></li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.heart-loading {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 200px;
  height: 200px;
  ul { 
    display: flex;
    justify-content: space-between;
    width: 150px;
    height: 150px; 
  }
  li {
    --0: calc(var(--line-index) / var(--line-count) * .5turn) ;
    --time: calc((var(--line-index) - 1) * 40ms);
    border-radius: 5px;
    width: 10px;
    height: 10px;
    background-color: #3c9;
    filter: hue-rotate(var(--0));
    animation-duration: 1s;
    animation-delay: var(--time);
    animation-iteration-count: infinite;
    &.line-1,
    &.line-9 {
      animation-name: beat1; 
    }
    &.line-2,
    &.line-8 {
      animation-name: beat2; 
    }
    &.line-3,
    &.line-7 {
      animation-name: beat3; 
    }
    &.line-4,
    &.line-6 {
      animation-name: beat4; 
    }
    &.line-5 {
      animation-name: beat5; 
    }
  }
}
@keyframes beat1 {
  0%,
  10%,
  90%,
  100% {
    height: 10px; 
  }  
  45%,
  55% {
    height: 30px;
    transform: translate3d(0, -15px, 0);
  }
}

@keyframes beat2 {
  0%,
  10%,
  90%,
  100% {
    height: 10px; 
  }  
  45%,
  55% {
    height: 60px;
    transform: translate3d(0, -30px, 0);
  }
}

@keyframes beat3 {
  0%,
  10%,
  90%,
  100% {
    height: 10px; 
  }  
  45%,
  55% {
    height: 80px;
    transform: translate3d(0, -40px, 0);
  }
}

@keyframes beat4 {
  0%,
  10%,
  90%,
  100% {
    height: 10px; 
  }  
  45%,
  55% {
    height: 90px;
    transform: translate3d(0, -30px, 0);
  }
}


@keyframes beat5 {
  0%,
  10%,
  90%,
  100% {
    height: 10px; 
  }  
  45%,
  55% {
    height: 90px;
    transform: translate3d(0, -20px, 0);
  }
}
</style>