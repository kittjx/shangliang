<template>
  <view class="commodity-item">
      <image class="commodity-pic" :src="commodity.pic" mode="widthFix"></image>
      <text class="commodity-text">{{ commodity.text }}</text>
      <view class="price-container">
        <text class="curpri">¥{{ commodity.curpri }}</text>
        <text class="oldpri">¥{{ commodity.oldpri }}</text>
      </view>
      <text class="discount">{{ commodity.discount }}</text>
    </view>
</template>

<script setup>

const props = defineProps({
  commodity: {
    type: Object,
    required: true
  }
});

</script>

<style lang="scss" scoped>

.commodity-item {
  width: 100%;
  box-sizing: border-box;
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 1upx; /* 可添加适当间距 */

  .commodity-pic {
    width: 100%;
    aspect-ratio: 1 / 1;
    object-fit: cover;
    border-radius: 8upx; /* 可选样式 */
  }

  .commodity-text {
    padding: 6upx 10upx;
    margin-top: 10upx;
    font-size: 24upx;
    display: -webkit-box;
    -webkit-box-orient: vertical;
    -webkit-line-clamp: 2;
    overflow: hidden;
    text-overflow: ellipsis;
    line-height: 1.5;
    height: calc(2 * 1.5em);
    width: 100%;
    text-align: center;
  }

  .price-container {
    width: 100%;
    padding: 0 10upx;
    margin-top: 8upx;
    display: flex;
    justify-content: center;
    align-items: center;
    
    .curpri {
      color: red;
      font-size: 28upx;
    }
    
    .oldpri {
      color: #999;
      font-size: 24upx;
      text-decoration: line-through;
      margin-left: 10upx;
    }
  }

  .discount {
    color: white;
    background-color: red;
    border-radius: 4upx;
    font-size: 24upx;
    padding: 2upx 8upx;
    margin-top: 8upx;
    align-self: flex-start;
    margin-left: 10upx;
    align-self: center;
  }
}

</style>