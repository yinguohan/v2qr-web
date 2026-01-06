<template>
  <view class="up-vid">
    <UploadVideo />
  </view>
</template>

<script setup>
import UploadVideo from "../../components/uploadVideo.vue";
</script>

<style scoped>
  .up-vid{
    display: flex;
    justify-content: center;
    /* 核心：向下平移屏幕高度的20% */
  transform: translateY(15vh);
  }
</style>
