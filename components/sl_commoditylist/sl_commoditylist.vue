<template>
  <view class="commoditylist">
    <sl_commodity class="commodity" v-for="(item, index) in commodities" :key="index" :commodity="item" />
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

.commodity {
  width: 50%;
}

</style>