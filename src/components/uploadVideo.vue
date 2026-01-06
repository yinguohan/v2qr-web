<template>
  <view class="upload-video-btn" @click="chooseVideo">
    <text class="iconfont">+</text>
    <text class="tips">点击上传视频</text>
  </view>
</template>

<script setup>
const chooseVideo = () => {
  uni.chooseMedia({
    count: 1,
    mediaType: ["video"],
    sourceType: ["album", "camera"],
    success: (res) => {
      console.log("选中视频", res.tempFiles[0].tempFilePath);
    },
  });
};
</script>

<style scoped>
.upload-video-btn {
  /* 放大尺寸：原180rpx → 280rpx，可按需调整 */
  width: 60vw;
  height: 60vw;
  /* 淡灰色边框：#e5e5e5 比原#ccc更淡 */
  border: 2rpx dashed #e5e5e5;
  border-radius: 16rpx; /* 圆角同步放大，更协调 */
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  /* 淡灰色背景：#fafafa 更浅 */
  background: #fafafa;
}
.iconfont {
  /* 加号放大：原60rpx → 80rpx */
  font-size: 80rpx;
  /* 淡灰色文字：#d0d0d0 更淡 */
  color: #d0d0d0;
  margin-bottom: 15rpx;
}
.tips {
  /* 文字放大：原24rpx → 28rpx */
  font-size: 28rpx;
  /* 文字颜色和加号一致，保持统一 */
  color: #d0d0d0;
}
/* 点击态也调淡，保持风格统一 */
.upload-video-btn:active {
  background: #f5f5f5;
}
</style>
