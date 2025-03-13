<template>
  <view class="commoditylist">
    
    <view class="commodity-item" v-for="(item, index) in commodities" :key="index">
      <image class="commodity-pic" :src="item.pic" mode="aspectFill"></image>
      <text class="commodity-text">{{item.text}}</text>
      <view>
        <text class="curpri">{{item.curpri}}</text>
        <text class="oldpri">{{item.oldpri}}</text>
      </view>
      <text class="discount">{{item.discount}}</text>
    </view>
    
  </view>
</template>

<script setup>

const props = defineProps({
  commodities: Array,
});

</script>

<style lang="scss" scoped>

.commoditylist {
  display: flex;
  flex-wrap: wrap;
}

.commodity-item {
  width: 50%; /* 每个商品占 50% 宽度 */
  box-sizing: border-box; /* 防止 padding 和 border 影响宽度 */
  display: flex;
  flex-direction: column; /* 垂直排列 */
  align-items: center; /* 内容水平居中 */
}

.commodity-pic {
  width: 100%;
  aspect-ratio: 1 / 1; /* 宽高比为 1:1，保持正方形 */
  object-fit: cover; /* 保持图片比例，裁剪多余部分 */
}

.commodity-text {
  margin-top: 1upx;
  font-size: 24upx;
  display: -webkit-box; /* 使用弹性盒子布局 */
  -webkit-box-orient: vertical; /* 垂直排列 */
  -webkit-line-clamp: 2; /* 限制显示两行 */
  overflow: hidden; /* 超出部分隐藏 */
  text-overflow: ellipsis; /* 超出部分显示省略号 */
  line-height: 1.5; /* 设置行高 */
  height: calc(2 * 1.5em); /* 固定高度为两行的高度 */
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
  border-radius: 4upx;
  font-size: 24upx;
}
</style>