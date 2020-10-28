<template>
  <AtTabBar fixed :tabList="tabList1" :on-click="tabBarClick" :current="current1" />
</template>

<script>
import Taro from "@tarojs/taro";
import { AtTabBar } from "taro-ui-vue";
export default {
  data() {
    return {
      current1: 3,
      tabList1: [
        { title: "首页", iconType: "bullet-list", text: "new" },
        { title: "喜欢", iconType: "heart" },
        { title: "消息", iconType: "streaming" },
        { title: "我的", iconType: "user", text: "100", max: 99 }
      ]
    };
  },
  components: {
    AtTabBar
  },
  methods: {
    tabBarClick(value) {
      this.current1 = value;
      switch (value) {
        case 0:
          Taro.redirectTo({
            url: "/pages/index/index"
          });
          break;
        case 1:
          Taro.redirectTo({
            url: "/pages/lick/lick"
          });
          break;
        case 2:
          Taro.redirectTo({
            url: "/pages/home/home"
          });
          break;
        case 3:
          Taro.redirectTo({
            url: "/pages/index/index"
          });
          break;
      }
    }
  }
};
</script>