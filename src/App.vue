<template>
  <div class="index-page">
    <div class="header flex-ct-y">
      <h1>
        <span class="gradient">iDea CSS</span>
        <img src="./assets/img/logo.svg" />
      </h1>
      <p>我是JowayYoung，一位重度CSS爱好者</p>
      <p>欢迎来到<strong class="vue">Pure CSS World</strong></p>
      <p>请往下滚动浏览更多好看实用的纯CSS特效👇</p>
      <p>依据美学标准将以下纯CSS特效划分为五大类</p>
      <p>布局-行为-色彩-图形-组件</p>
      <p>大部分纯CSS特效为原创，亦有少部分参考他人</p>
      <p>2019年在掘金社区发布一篇纯CSS特效文章</p>
      <p>目前已斩获4000+点赞量和110k+阅读量</p>
      <p>稳居掘金社区点赞量前10排行榜并深受好评</p>
      <p>若你有更多想象空间也可贡献出你的iDea CSS❤️</p>
      <p>
        目前已发布<strong class="default">{{ count }}</strong
        >个，争取每周更新<strong class="react">1~2</strong>个
      </p>
      <p>CSS没有想象中的简单也没有实际中的难用</p>
      <p>为了让更多开发者关注CSS，一起Star该项目好吗😜</p>
      <div>
        <iframe
          src="https://ghbtns.com/github-btn.html?user=JowayYoung&repo=idea-css&type=star&count=true&size=large"
          frameborder="0"
          scrolling="0"
          width="130"
          height="30"
          title="GitHub"
        ></iframe>
        <iframe
          src="https://ghbtns.com/github-btn.html?user=JowayYoung&repo=idea-css&type=fork&count=true&size=large"
          frameborder="0"
          scrolling="0"
          width="130"
          height="30"
          title="GitHub"
        ></iframe>
        <iframe
          src="https://ghbtns.com/github-btn.html?user=JowayYoung&repo=idea-css&type=watch&count=true&size=large&v=2"
          frameborder="0"
          scrolling="0"
          width="140"
          height="30"
          title="GitHub"
        ></iframe>
      </div>
    </div>
    <div class="content layout">
      <layout></layout>
      <layout1></layout1>
      <layout2></layout2>
      <layout3></layout3>
      <layout4></layout4>
      <layout5></layout5>
      <layout6></layout6>
      <layout7></layout7>
      <layout8></layout8>
      <layout9></layout9>
      <layout10></layout10>
    </div>
    <div class="content behavior">
      <behavior1></behavior1>
      <behavior2></behavior2>
      <behavior3></behavior3>
      <behavior4></behavior4>
      <behavior5></behavior5>
      <behavior6></behavior6>
      <behavior7></behavior7>
      <behavior8></behavior8>
      <behavior9></behavior9>
      <behavior10></behavior10>
      <behavior11></behavior11>
      <behavior12></behavior12>
      <behavior13></behavior13>
      <behavior14></behavior14>
      <behavior15></behavior15>
      <behavior16></behavior16>
      <behavior17></behavior17>
      <behavior18></behavior18>
      <behavior19></behavior19>
      <behavior20></behavior20>
      <behavior21></behavior21>
    </div>
    <div class="content color">
      <color1></color1>
      <color2></color2>
      <color3></color3>
      <color4></color4>
      <color5></color5>
      <color6></color6>
      <color7></color7>
      <color8></color8>
      <color9></color9>
      <color10></color10>
      <color11></color11>
      <color12></color12>
    </div>
    <div class="content figure">
      <figure1></figure1>
      <figure2></figure2>
      <figure3></figure3>
      <figure4></figure4>
      <figure5></figure5>
      <figure6></figure6>
      <figure7></figure7>
      <figure8></figure8>
      <figure9></figure9>
      <figure10></figure10>
      <figure11></figure11>
      <figure12></figure12>
    </div>
    <div class="content component">
      <component1></component1>
      <component2></component2>
      <component3></component3>
      <component4></component4>
      <component5></component5>
      <component6></component6>
      <component7></component7>
      <component8></component8>
      <component9></component9>
      <component10></component10>
      <component11></component11>
      <component12></component12>
      <component13></component13>
      <component14></component14>
      <component15></component15>
      <component16></component16>
      <component17></component17>
      <component18></component18>
      <component19></component19>
      <component20></component20>
      <component21></component21>
      <component22></component22>
      <component23></component23>
      <component24></component24>
      <component25></component25>
      <component26></component26>
      <component27></component27>
      <component28></component28>
      <component29></component29>
      <component30></component30>
      <component31></component31>
      <component32></component32>
      <component33></component33>
      <component34></component34>
    </div>
  </div>
</template>

<style lang="scss">
::-webkit-scrollbar {
  width: 6px;
  height: 6px;
}
::-webkit-scrollbar-track {
  background-color: rgba(#ccc, 0.3);
}
::-webkit-scrollbar-thumb {
  border-radius: 3px;
  background-color: #ccc;
}
.header {
  overflow: hidden;
  height: 100vh;
  background-color: #282c34;
  h1 {
    margin: 20px 0;
    font-size: 10vmin;
  }
  img {
    display: inline-block;
    height: 10vmin;
    vertical-align: super;
    animation: swing 3s infinite;
  }
  p {
    line-height: 1.5;
    font-size: 1.8vmin;
    color: #fff;
    & + p {
      margin-top: 10px;
    }
  }
  strong {
    display: inline-block;
    margin: 0 3px;
    padding: 0 6px;
    border-radius: 5px;
    line-height: 20px;
    color: #fff;
    &.default {
      background-color: #f66;
    }
    &.react {
      background-color: #61dafb;
    }
    &.vue {
      background-color: #42b983;
    }
  }
  div {
    display: flex;
    margin-top: 20px;
  }
  .gradient {
    background-image: linear-gradient(92deg, #f66 0%, #f90 100%);
    background-clip: text;
    color: #f66;
    animation: hue 5s infinite linear;
    -webkit-text-fill-color: transparent;
  }
}
.bruce {
  overflow: hidden;
  position: relative;
  padding: 50px 0;
  border-bottom: 1px solid #ccc;
  min-height: 300px;
  &::before {
    position: absolute;
    left: 50%;
    top: 0;
    z-index: 99999;
    padding: 0 10px;
    border-radius: 0 0 5px 5px;
    max-width: 300px;
    line-height: 20px;
    color: #fff;
    content: attr(data-title);
    transform: translateX(-50%);
  }
  &::after {
    position: absolute;
    right: 0;
    bottom: 0;
    z-index: 99999;
    padding: 5px 10px;
    border-top-left-radius: 5px;
    background-color: #ccc;
    font-weight: bold;
    font-size: 16px;
    color: #fff;
  }
}
.content {
  overflow: auto;
  transition: all 300ms;
  &.layout .bruce {
    &::before {
      background-color: #f66;
    }
    &::after {
      content: "布局";
    }
  }
  &.behavior .bruce {
    &::before {
      background-color: #66f;
    }
    &::after {
      content: "行为";
    }
  }
  &.color .bruce {
    &::before {
      background-color: #f90;
    }
    &::after {
      content: "颜色";
    }
  }
  &.figure .bruce {
    &::before {
      background-color: #09f;
    }
    &::after {
      content: "图形";
    }
  }
  &.component .bruce {
    &::before {
      background-color: #3c9;
    }
    &::after {
      content: "组件";
    }
  }
}
@keyframes hue {
  from {
    filter: hue-rotate(0);
  }
  to {
    filter: hue-rotate(-360deg);
  }
}
@keyframes swing {
  0%,
  65% {
    transform: rotate(0);
  }
  70% {
    transform: rotate(6deg);
  }
  75% {
    transform: rotate(-6deg);
  }
  80% {
    transform: rotate(6deg);
  }
  85% {
    transform: rotate(-6deg);
  }
  90% {
    transform: rotate(6deg);
  }
  95% {
    transform: rotate(-6deg);
  }
  100% {
    transform: rotate(0);
  }
}
</style>

<script>
import Layout from './components/layout/use-margin.vue'
import Layout2 from "./components/layout/use-flexbox.vue";
import Behavior12 from './components/behavior/use-attr-node-property.vue'
import Component7 from './components/component/use-counter-interator.vue'
import Component22 from './components/component/bar-loading.vue'
import Component24 from './components/component/heart-shaped-loading.vue'
import Figure3 from './components/figure/use-clip-path.vue'
export default {
  name: "app",
  components: {
    // 组件
    Component7,
    Component22,
    Component24,
    // 行为
    Behavior12,
    // 布局
    Layout,
    Layout2,
    // 图形
    Figure3
  },
  data() {
    return {
      count: 0,
    };
  },
  mounted() {
    const items = document.getElementsByClassName("bruce") || [];
    this.count = items.length;
  },
};
</script>