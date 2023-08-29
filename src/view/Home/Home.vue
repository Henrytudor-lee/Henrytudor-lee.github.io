<script setup lang="ts">
import { reactive } from "vue";
const imgDataList = reactive([
  {
    img: "/images/pink.jpg",
    from: "https://500px.com/photo/273810919/pink-sands-by-jack-hopkins",
  },
  {
    img: "/images/white.jpg",
    from: "https://500px.com/photo/222636895/bad-hair-day-by-bea-burin-herbst",
  },
  {
    img: "/images/blue.jpg",
    from: "https://500px.com/photo/1043856879/eba-by-my-world-vision-carlos-infante-luna",
  },
  {
    img: "/images/yellow.jpg",
    from: "https://500px.com/photo/214066731/yellow-memory-ii-by-milan-vopalensky",
  },
  {
    img: "/images/red.jpg",
    from: "https://500px.com/photo/1040154522/red-temple-in-the-dark-by-vitaly-tyuk",
  },
]);
</script>

<template>
  <div class="home">
    <div class="top">
      <div class="img-card" v-for="item in imgDataList">
        <img :src="item.img" :alt="item.from" />
      </div>
      <div class="title logo-title">Garcia World</div>
      <div class="nav-bar"></div>
      <div class="top-button"></div>
    </div>
    <div class="bottom">
      <h5 class="text-title">About Me</h5>
      <div class="text-content">
        <div class="img">
          <img src="" alt="">
        </div>
        <div class="text text-main">
          我叫xx，是x年级的学生。身高xxx，是个勤恳读书，热爱集体，遵守纪律的学生，在老师同学们的帮助下，我有了一定的进步，老师同学们也不时地鼓励我，也取得了一点成绩。我们是毕业班，肩负着“为校争光”的`责任。不用说我和大家一样，不会辜负学校的栽培，和家长的殷切期望，在校认真听讲遵守纪律，在家认真复习功课，不玩电脑游戏。用实际行动，让师长们和家长放心。谢谢大家！
        </div>
      </div>
      <div class="sub-content">ABCFDAFASD</div>
    </div>
  </div>
</template>

<style lang="less">
.home {
  width: 100%;
  display: flex;
  flex-direction: column;
  .top {
    height: 450px;
    background-color: lightblue;
    overflow: hidden;
    display: flex;
    position: relative;
    .img-card {
      flex: 1;
      background-color: #e3e3e3;
      padding: 8px;
      filter: blur(2px);
      img {
        width: 100%;
      }
    }
    .title,
    .nav-bar,
    .top-button {
      position: absolute;
    }
    .title {
      left: 0;
      right: 0;
      top: 0;
      bottom: 0;
      margin: auto;
      width: 500px;
      height: 80px;
      line-height: 80px;
      text-align: center;
      background-color: #ccc;
      opacity: 0.7;
      border-radius: 20px;
      box-shadow: 0px 4px 10px 0px rgba(0, 0, 0, 0.3);
      &:hover {
        background-color: #6b6b6b;
        box-shadow: 0px 4px 10px 0px rgba(0, 0, 0, 0.8);
        opacity: 1;
        cursor: pointer;
      }
    }
  }
  .bottom {
    height: 360px;
    padding: 20px;
    display: flex;
    flex-direction: column;
    .text-content {
      height: 100%;
      // background-color: cadetblue;
      display: flex;
      .img{
        width: 260px;
        background-color: cadetblue;
        margin-right: 20px;
      }
      .text{
        flex: 1;
      }
    }
    .sub-content {
      height: 40px;
      // background-color: chocolate;
      line-height: 50px;
      font-size: 18px;
      font-family: Arial, Helvetica, sans-serif;
      text-align: center;
    }
  }
}
</style>
