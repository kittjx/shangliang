<template>
  <view class="commodity">
    <view class="commodity-item">
      <image class="commodity-pic" src="/static/pic/commodity1.jpg" mode="aspectFit"></image>
      <view class="commodity-content">
        <text class="commodity-text">这是商品1的介绍,快来买啊,必须买</text>
      </view>
      <view>
        <text class="curpri">$199</text>
        <text class="oldpri">$599</text>
      </view>
      <text class="discount">2.8折</text>
    </view>
    
    <view class="commodity-item">
      <image class="commodity-pic" src="/static/pic/commodity1.jpg" mode="aspectFit"></image>
      <view class="commodity-content">
        <text class="commodity-text">这是商品1的介绍,快来买啊,必须买</text>
      </view>
      <view>
        <text class="curpri">$199</text>
        <text class="oldpri">$599</text>
      </view>
      <text class="discount">2.8折</text>
    </view>
    
  </view>
  
</template>

<script setup>

</script>

<style lang="scss" scoped>
  
  .commodity {
    display: flex;
    flex-wrap: wrap;
  }

  .commodity-item {
    width: 50%; /* 每个商品占 50% 宽度 */
    box-sizing: border-box; /* 防止 padding 和 border 影响宽度 */
    padding-bottom: 10upx;
    display: flex;
    flex-direction: column; /* 垂直排列 */
    align-items: center; /* 内容水平居中 */
  }

  .commodity-pic {
    width: 100%;
    aspect-ratio: 1 / 1; /* 宽高比为 1:1，保持正方形 */
    object-fit: cover; /* 保持图片比例，裁剪多余部分 */
  }
  
  .commodity-content {
    margin-top: 10upx;
  }
  
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
  
  .discount {
    color: white;
    background-color: red;
    padding: 4upx 8upx;
    border-radius: 4upx;
    font-size: 24upx;
    margin-left: 10upx;
  }
</style>