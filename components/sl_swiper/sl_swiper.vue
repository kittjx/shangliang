<template>
  <view class="swiper-container">
    <swiper 
      class="swiper" 
      autoplay="true" 
      interval="3000" 
      duration="1000" 
      circular="true" 
      indicator-dots="true">
      
      <swiper-item v-for="(item, index) in images" :key="index">
        <view class="swiper-item">
          <image :src="item" mode="aspectFit" class="swiper-pic" />
        </view>
      </swiper-item>

    </swiper>
  </view>
</template>

<script setup>

defineProps({
  images: {
    type: Array,
    required: true
  }
});

</script>

<style lang="scss" scoped>
  
.swiper-container {
  width: 100%;
  height: 350upx;
  display: flex;
  justify-content: center;
  align-items: center;
}

.swiper {
  width: 100%;
  height: 100%;
}

.swiper-item {
  width: 100%;
  height: 100%;
  background-color: #f0f0f0;
  color: #333;
  font-size: 24upx;
  border-radius: 10upx;
}

.uni-swiper-dot {
  width: 8upx;
  height: 8upx;
  background-color: #999;
  border-radius: 50%;
  transition: background-color 0.3s;
}
 
.uni-swiper-dot-active {
  background-color: #007aff;
}

.swiper-pic {
  width: 100%;
  height: 100%;
  justify-content: center;
  align-items: center;
}
  
</style>