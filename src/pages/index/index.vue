<template>
  <view class="index">
    <nut-button type="primary" @click="onClick">按钮111</nut-button>
    <nut-toast v-model:visible="show" msg="哈哈哈" type="text"></nut-toast>
  </view>
</template>

<script setup>
import { ref } from "vue";
import Taro from "@tarojs/taro";

const show = ref(false);
const onClick = () => {
  Taro.showToast({
    title: "成功",
    icon: "success",
    duration: 2000,
  });
};
</script>
