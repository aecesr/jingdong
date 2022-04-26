<template>
  <div class="docker">
    <!-- 底部導航 -->
    <div class="docker">
      <!-- BEM block__element--modifier -->
      <div class="docker__item docker__item--active">
        <div class="iconfont">&#xe626;</div>
        <div class="docker__title">首页</div>
      </div>

      <div class="docker__item">
        <div class="iconfont">&#xe7d6;</div>
        <div class="docker__title">购物车</div>
      </div>
      <div class="docker__item">
        <div class="iconfont">&#xe61f;</div>
        <div class="docker__title">订单</div>
      </div>
      <div class="docker__item">
        <div class="iconfont">&#xe7d5;</div>
        <div class="docker__title">我的</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" soped>
@import "../style/index.scss";
.docker {
  display: flex;
  position: absolute;
  width: 100vw;
  height: 0.49rem;
  border-top: 0.01rem solid #f1f1f1;
  left: 0;
  bottom: 0;
  /*background-color: red; */
  color: $content-fontcolor;
  &__item {
    flex: 1;
    text-align: center;
    .iconfont {
      margin: 0.07rem 0 0.02rem 0;
      font-size: 0.18rem;
    }
    &--active {
      color: $hightlight-color;
    }
  }
  &__title {
    font-size: 0.2rem;
    transform: scale(0.5, 0.5);
    transform-origin: center, top;
  }
}
</style>