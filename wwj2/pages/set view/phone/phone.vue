<template>
  <view class="container">
    <view class="input-area">
      <view class="title">请输入你的新手机号</view>
      <view class="input-wrapper">
        <input type="number" class="input-box" />
      </view>
    </view>
    <button class="confirm-button">确认更改</button>
  </view>
</template>

<script>
export default {
  data() {
    return {};
  },
};
</script>

<style scoped>
.container {
  margin: 20px;
}

.input-area {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-bottom: 20px;
}

.title {
  font-weight: bold;
  font-size: 18px;
  margin-bottom: 10px;
}

.input-wrapper {
  width: 300px;
  border: 1px solid #ccc;
  border-radius: 5px;
  padding: 5px;
}

.input-box {
  width: 100%;
  border: none;
  outline: none;
}

.confirm-button {
  padding: 10px 20px;
  background-color: #e6e6e6;
  border-radius: 5px;
}
</style>
