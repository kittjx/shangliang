<template>
  <view class="window">
    <view class="title-container">
      <view>-</view>
      <view class="window-title">{{title}}</view>
      <view>-</view>
    </view>
    <view class="commodity-container">
      <sl_commoditylist></sl_commoditylist>
    </view>
  </view>
</template>

<script setup>
  
defineProps({
  title: {
    type: String,
    required: true
  }
});

</script>

<style lang="scss" scoped>

.window {
  padding: 20upx 0;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: flex-start;
  font-weight: bold;
  padding: 10upx;
  
  .window-title {
    padding: 0 20upx;
    font-size: 32upx;
  }
}
</style>