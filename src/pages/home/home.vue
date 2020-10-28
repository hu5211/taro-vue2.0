<template>
  <view class="index">
    <Header />
    <Swiper />
    <!-- <AtButton type="primary" :on-click="handleClick">路由跳转</AtButton> -->
    <Footer />
  </view>
</template>

<script>
import Taro from "@tarojs/taro";
import { AtButton } from "taro-ui-vue";
import Header from "../components/header";
import Swiper from "../components/swiper";
import Footer from "../components/footer";
import "./home.scss";
export default {
  components: {
    AtButton,
    Header,
    Swiper,
    Footer
  },
  data() {
    return {};
  },
  methods: {
    handleClick() {
      Taro.navigateTo({
        url: "/pages/index/index"
      });
    }
  }
};
</script>
