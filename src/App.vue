<template>
  <div>
    <!-- 顶部搜索 -->
    <div class="wrapper">
      <div class="wrapper__position">
        <span class="iconfont">&#xe64c;</span>
        南京工业职业技术大学计算机与软件学院软件工程技术本科专业2021级
        <span class="iconfont wrapper__position__notice">&#xe7c4;</span>
      </div>

      <!-- 搜索 -->
      <div class="wrapper__search">
        <span class="iconfont">&#xe7da;</span>
        <span class="search__text">山姆会员商店优惠商品</span>
      </div>

      <div class="wrapper__banner">
        <img
          src="https://chl-bucket.oss-cn-hangzhou.aliyuncs.com/md/202204251435492.jpeg"
          class="wrapper__banner__img"
          alt=""
        />
      </div>
    </div>

    <!-- icons九宫格区 -->

    <!-- gap -->
    <div class="gap"></div>
    <docker></docker>
  </div>
</template>

<script>
import Docker from "./components/Docker.vue";
export default {
  components: {
    Docker
  },
  data() {
    return {};
  },
};
</script>
<style lang="scss" soped>
@import './style/index.scss';
.wrapper {
  position: absolute;
  left: 0;
  right: 0;
  top: 0;
  bottom: 0.5rem;
  padding: 0 0.18rem;
  &__position {
    position: relative;
    padding: 0.16rem 0.16rem 0.16rem 0;
    font-size: 0.16rem;
    // background: greenyellow;
    @include ellipse;
    &__notice {
      position: absolute;
      right: 0;
      // top: 0.1rem;
      // font-size: 0.2rem;
    }
    color: $content-fontcolor;
  }
  &__search {
    margin-bottom: 0.12rem;
    line-height: 0.32rem;
    background-color: $background-color;
    color: $placeholder-fontcolor;
    border-radius: 0.16rem;
    .iconfont {
      display: inline-block;
      padding: 0 0.12rem 0 0.16rem;
      font-style: 0.2rem;
    }
    &__text {
      display: inline-block;
      font-size: 0.14rem;
    }
  }
  &__banner {
    // hack技巧：预留出高度防抖，(图片高/宽)
    height: 0;
    overflow: hidden;
    padding-bottom: 25.4%;
    &__img {
      width: 100%;
    }
  }
}
</style>
