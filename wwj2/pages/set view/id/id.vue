<template>
  <view class="container">
    <view class="viewbox">
      <view class="left">姓名</view>
      <view class="right">
        <text>姓名数据</text>
      </view>
    </view>

    <view class="viewbox">
      <view class="left">身份证号</view>
      <view class="right">
        <text>身份证数据</text>
      </view>
    </view>

    <text class="note">实名认证信息无法更改，若要更改请联系客服</text>

    <button class="button">返回</button>
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

.viewbox {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 10px;
}

.left {
  font-weight: bold;
}

.note {
  margin-top: 20px;
  color: grey;
}

.button {
  margin-top: 20px;
  padding: 10px 20px;
  background-color: #e6e6e6;
  border-radius: 5px;
}
</style>
