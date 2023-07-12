<template>
	<view style="position: fixed;top: 40rpx;width: 100%;">
		<!-- 顶部导航栏 -->
		<view style="display: flex;justify-content: center;align-items: center;">
			<view style="position: absolute;left: 0rpx;">
				<uni-icons type="search" size="30"></uni-icons>
			</view>
			<text class="daohanglan-text">关注</text>
			<text class="daohanglan-text">推荐</text>
			<text class="daohanglan-text">附近</text>
			<view style="position: absolute;right: 0rpx;">
				<uni-icons type="plus" size="30"></uni-icons>
			</view>
		</view>
		<!-- 内容 -->
		<view class="content">
			<swiper vertical="true" class="contentlist">
				<swiper-item v-for="(item,index) in 6">
					<view>
					<image class="contentlist-mage" src="../../static/logo.png" mode="aspectFill" style="width: 100%;"></image>
					</view>
				</swiper-item>
			</swiper>
			<view>
				<text>1111</text>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				newsList: [{
						title: '资讯标题1',
						content: '资讯内容1'
					},
					{
						title: '资讯标题2',
						content: '资讯内容2'
					},
					{
						title: '资讯标题3',
						content: '资讯内容3'
					},
					{
						title: '资讯标题4',
						content: '资讯内容4'
					},
					{
						title: '资讯标题5',
						content: '资讯内容5'
					},
				],
			};
		},
	};
</script>


<style>
	/* 导航栏标题内容 */
	.daohanglan-text {
		font-size: 40rpx;
		margin: 20rpx;
	}
	.content{
		height: 100vh;
	}
	.contentlist{
		height: 400rpx;
		margin: 100rpx;
	}
	.contentlist-mage{
		width: 100%;
		border:1rpx solid #000000;
		border-radius: 90rpx;
	}
</style>