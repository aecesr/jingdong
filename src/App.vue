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
      <!-- icons九宫格区 -->
      <icons :Icons="icons"></icons>

    </div>

    

    

    <!-- gap -->
    <div class="gap"></div>
    <docker></docker>
  </div>
</template>

<script>
import Icons from "./components/Icons.vue"
import Docker from "./components/Docker.vue";
export default {
  components: {
    Docker,
    Icons
  },
  data() {
    return {
      icons:[
        {
          title:"超市便利",
          img:"https://chl-bucket.oss-cn-hangzhou.aliyuncs.com/icon/icon/%E8%B6%85%E5%B8%82.png",
        },
        {
          title:"菜市场",
          img:"https://chl-bucket.oss-cn-hangzhou.aliyuncs.com/icon/icon/%E8%8F%9C%E5%B8%82%E5%9C%BA.png",
        },
        {
          title:"水果店",
          img:"https://chl-bucket.oss-cn-hangzhou.aliyuncs.com/icon/icon/%E6%B0%B4%E6%9E%9C%E5%BA%97.png",
        },
        {
          title:"鲜花绿植",
          img:"https://chl-bucket.oss-cn-hangzhou.aliyuncs.com/icon/icon/%E9%B2%9C%E8%8A%B1.png",
        },
        {
          title:"医药健康",
          img:"https://chl-bucket.oss-cn-hangzhou.aliyuncs.com/icon/icon/%E5%8C%BB%E8%8D%AF%E5%81%A5%E5%BA%B7.png",
        },
        {
          title:"家居时尚",
          img:"https://chl-bucket.oss-cn-hangzhou.aliyuncs.com/icon/icon/%E5%AE%B6%E5%B1%85.png",
        },
        {
          title:"烘焙蛋糕",
          img:"https://chl-bucket.oss-cn-hangzhou.aliyuncs.com/icon/icon/%E8%9B%8B%E7%B3%95.png",
        },
        {
          title:"签到",
          img:"https://chl-bucket.oss-cn-hangzhou.aliyuncs.com/icon/icon/%E7%AD%BE%E5%88%B0.png",
        },
        {
          title:"大牌免运",
          img:"https://chl-bucket.oss-cn-hangzhou.aliyuncs.com/icon/icon/%E5%A4%A7%E7%89%8C%E5%85%8D%E8%BF%90.png",
        },
        {
          title:"红包套餐",
          img:"https://chl-bucket.oss-cn-hangzhou.aliyuncs.com/icon/icon/%E7%BA%A2%E5%8C%85.png",
        },
      ],
    };
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
.icons {
  display: flex;
  flex-wrap: wrap;
  margin-top: 0.16rem;
  &__item {
    // display: block;
    width: 20%;
    &__img {
      display: block;
      width: 0.4rem;
      height: 0.4rem;
      margin: 0 auto;
    }
    &__desc {
      margin: 0.06rem 0 0.16rem 0;
      text-align: center;
      color: $content-fontcolor;
    }
  }
}
</style>
