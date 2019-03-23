<template>
  <div class="tuijian">
    <div class="bg"></div>
    <mt-swipe class="tuijian-swiper" :auto="5000">
      <mt-swipe-item v-for="(v,i) in swiperList" :key="i" class="tuijian-swiper-item">
        <img :src="v.src">
      </mt-swipe-item>
    </mt-swipe>
  </div>
</template>

<script>
import { Swipe, SwipeItem } from "mint-ui";
export default {
  components: {
    "mt-swipe": Swipe,
    "mt-swipe-item": SwipeItem
  },
  data() {
    return {
      swiperList: [
        {
          src: "/img/s1.jpg"
        },
        {
          src: "/img/s2.jpg"
        },
        {
          src: "/img/s3.jpg"
        },
        {
          src: "/img/s4.jpg"
        },
        {
          src: "/img/s5.jpg"
        },
        {
          src: "/img/s6.jpg"
        }
      ]
    };
  }
};
</script>

<style lang="less" scoped>
.tuijian {
  position: relative;
  .bg {
    .h(300);
    background: linear-gradient(to bottom, #e8493d, #ff594a);
    position: absolute;
    top: -1px;
    width: 100%;
  }
  .tuijian-swiper {
    .h(440);
    .tuijian-swiper-item {
      .p(20);
      box-sizing: border-box;
      img {
          width: 100%;
          height: 100%;
          .br(20);
      }
    }
  }
}
</style>

