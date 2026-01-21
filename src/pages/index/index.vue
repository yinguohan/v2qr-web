<template>
  <view class="up-vid">
    <UploadVideo />
  </view>
  <view class="btn-submit">
    <button class="btn-generate-qrCode">生成二维码</button>
  </view>
</template>

<script setup>
import UploadVideo from "../../components/uploadVideo.vue";
</script>

<style scoped>

  /* 上传视频+号按钮 */
.up-vid {
  display: flex;
  justify-content: center;
  /* 核心：向下平移屏幕高度的20% */
  transform: translateY(15vh);
}
/* 生成二维码按钮 */
.btn-generate-qrCode {
  width: 70%;
  background-color: #007aff;
  color: #ffffff;
}
/* 控制按钮位置 */
.btn-submit{
  display: flex;
  margin-bottom: 20%
}
</style>
