<template>
  <div class="bruce flex-ct-x" data-title="使用传统方式排版各重布局">
    <div class="layout-box">
      <div class="full-screen-layout" title="使用postion+left/right/top/bottom">
        <header></header>
        <main></main>
        <footer></footer>
      </div>
      <div class="two-column-layout-float" title="使用float实现现布局">
        <div class="left"></div>
        <div class="right"></div>
      </div>
      <div class="two-column-layout-overflow" title="overflow+float">
        <div class="left"></div>
        <div class="right"></div>
      </div>
      <div class="three-column-layout" title="overflow+flow">
        <div class="left"></div>
        <div class="center"></div>
        <div class="right"></div>
      </div>
      <div class="grail-layout">
        <div class="left"></div>
        <div class="right"></div>
        <div class="center"></div>
      </div>
      <div class="double-wing">
        <div class="left"></div>
        <div class="right"></div>
        <div class="center">
          <div></div>
        </div>
      </div>
      <div class="average-layout-float">
        <div class="one"></div>
        <div class="two"></div>
        <div class="three"></div>
        <div class="four"></div>
      </div>
      <div class="average-layout-column">
        <div class="one"></div>
        <div class="two"></div>
        <div class="three"></div>
        <div class="four"></div>
      </div>
      <div class="center-layout-inline-block">
        <div></div>
      </div>
      <div class="center-layout-table-cell">
        <div></div>
      </div>
      <div class="center-layout-position">
        <div></div>
      </div>
      <div class="center-layout-simple">
        <div></div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.layout-box {
  display: flex;
  overflow-x: auto;
  flex-flow: nowrap;
  justify-content: space-between;
  margin: 0 50px;
  > div {
    flex-shrink: 0;
    flex-basis: 400px;
    & + div {
      margin-left: 50px;
    }
  }
}
.full-screen-layout {
  position: relative;
  width: 400px;
  height: 400px;
  header,
  footer,
  main {
    position: absolute;
    left: 0;
    right: 0;
  }
  header {
    top: 0;
    height: 50px;
    background-color: #f66;
  }
  footer {
    bottom: 0;
    height: 50px;
    background-color: #66f;
  }
  main {
    top: 50px;
    bottom: 50px;
    background-color: #3c9;
  }
}
.two-column-layout-float {
  width: 400px;
  height: 400px;
  .left {
    float: left;
    width: 100px;
    height: 100%;
    background-color: #f66;
  }
  .right {
    margin-left: 100px;
    height: 100%;
    background-color: #66f;
  }
}
.two-column-layout-overflow {
  width: 400px;
  height: 400px;
  .left {
    float: left;
    width: 100px;
    height: 100%;
    background-color: #f66;
  }
  .right {
    overflow: hidden;
    height: 100%;
    background-color: #66f;
  }
}
.three-column-layout {
  width: 400px;
  height: 400px;
  .left {
    float: left;
    width: 50px;
    height: 100%;
    background-color: #f66;
  }
  .center {
    float: left;
    width: 100px;
    height: 100%;
    background-color: #66f;
  }
  .right {
    overflow: hidden;
    height: 100%;
    background-color: #3c9;
  }
}
.grail-layout {
  padding: 0 100px;
  width: 400px;
  height: 400px;
  .left {
    float: left;
    margin-left: -100px;
    width: 100px;
    height: 100%;
    background-color: #f66;
  }
  .right {
    float: right;
    margin-right: -100px;
    width: 100px;
    height: 100%;
    background-color: #66f;
  }
  .center {
    height: 100%;
    background-color: #3c9;
  }
}
.double-wing {
  width: 400px;
  height: 400px;
  .left {
    float: left;
    width: 100px;
    height: 100%;
    background-color: #f66;
  }
  .right {
    float: right;
    width: 100px;
    height: 100%;
    background-color: #66f;
  }
  .center {
    margin: 0 100px;
    height: 100%;
    background-color: #3c9;
  }
}
.average-layout-float,
.average-layout-column {
  width: 400px;
  height: 400px;
  .one {
    background-color: #f66;
  }
  .two {
    background-color: #66f;
  }
  .three {
    background-color: #f90;
  }
  .four {
    background-color: #09f;
  }
}
.average-layout-float {
  > div {
    float: left;
    width: 25%;
    height: 100%;
  }
}
.average-layout-column {
  column-count: 4;
  column-gap: 0;
  width: 400px;
  height: 400px;
  > div {
    height: 100%;
  }
}
.center-layout-inline-block,
.center-layout-table-cell,
.center-layout-position,
.center-layout-simple {
  width: 400px;
  height: 400px;
  background-color: #f66;
  > div {
    width: 100px;
    height: 100px;
    background-color: #66f;
  }
}

.center-layout-inline-block {
  line-height: 400px;
  text-align: center;
  font-size: 0;
  div {
    display: inline-block;
    vertical-align: middle;
  }
}
.center-layout-table-cell {
  display: table-cell;
  vertical-align: middle;
  > div {
    margin: 0 auto;
  }
}
.center-layout-position {
  position: relative;
  > div {
    position: absolute;
    left: 50%;
    right: 50%;
    // margin: -50px 0 0 -50px;
    transform: translate(-50%, -50%);
  }
}
.center-layout-simple {
  display: flex;
  > div {
    margin: auto;
  }
}
</style>