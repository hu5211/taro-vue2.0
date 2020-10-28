<template>
  <view class="index">
    <Header />
    {{lick}}
    <Footer />
  </view>
</template>

<script>
import Taro from "@tarojs/taro";
import { AtButton } from "taro-ui-vue";
import Header from "../components/header";
import Footer from "../components/footer";
import "./lick.scss";
export default {
  components: {
    AtButton,
    Header,
    Footer
  },
  data() {
    return {
      lick: "喜欢"
    };
  }
};
</script>
