<template>
  <view>
    <sl_swiper :images="imageList"></sl_swiper>
    <sl_showcase title="热销爆品" :commodities="commodities"></sl_showcase>
    <sl_showcase title="为您推荐" :commodities="commodities"></sl_showcase>
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

const commodities = [
  {
    pic: "/static/pic/commodity1.jpg",
    text: "商品1,爆款,快来买啊,必须买,晚了就没有里,买买买买买买买买买买买买买买买买买买买买买买买买",
    curpri: "100",
    oldpri: "200",
    discount: "2折"
  },
  {
    pic: "/static/pic/commodity2.jpg",
    text: "商品2",
    curpri: "200",
    oldpri: "500",
    discount: "4折"
  },
  {
    pic: "/static/pic/commodity3.jpg",
    text: "商品3",
    curpri: "200",
    oldpri: "500",
    discount: "4折"
  },
  {
    pic: "/static/pic/commodity4.jpg",
    text: "商品4",
    curpri: "200",
    oldpri: "500",
    discount: "4折"
  },
]

</script>

<style lang="scss" scoped>

</style>