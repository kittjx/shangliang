<template>
  <view>
    <sl_swiper :images="imageList"></sl_swiper>
    <sl_showcase title="热销爆品"></sl_showcase>
    <sl_showcase title="为您推荐"></sl_showcase>
  </view>
</template>

<script setup>

const imageList = [
  '/static/pic/banner1.jpg',
  '/static/pic/banner2.jpg',
  '/static/pic/banner3.jpg',
  '/static/pic/banner4.jpg',
  '/static/pic/banner5.jpg'
];

</script>

<style lang="scss" scoped>

</style>