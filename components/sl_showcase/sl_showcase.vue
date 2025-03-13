<template>
  <view class="window">
    <view class="title-container">
      <view>-</view>
      <view class="window-title">{{title}}</view>
      <view>-</view>
    </view>
    <view class="commodity-container">
      <sl_commoditylist :commodities="commodities"></sl_commoditylist>
    </view>
  </view>
</template>

<script setup>
  
defineProps({
  title: {
    type: String,
    required: true
  },
  commodities: {
    type: Array,
    required: true
  }
});

</script>

<style lang="scss" scoped>

.window {
  width: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.title-container {
  display: flex;
  align-items: center;
  justify-content: center;
}

.window-title {
  font-size: 32upx;
  font-weight: bold;
}

</style>