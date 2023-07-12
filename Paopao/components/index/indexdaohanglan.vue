<template>
	<view>
		<uni-nav-bar style="height: 30px" :fixed="true" :border="false" left-width="50rpx" right-width="50rpx">
			<view slot="left">
				<uni-icons type="search" size="24"></uni-icons>
			</view>
			<scroll-view scroll-x="true" :scroll-into-view='scrollIntoIndex'>
				<view style="display: flex;flex-direction: row;justify-content: center;align-items: center;">
					<view class='scroll-item'>
						<text style="font-size: 40rpx;padding: 20rpx;">关注</text>
					</view>
					<view class='scroll-item'>
						<text style="font-size: 40rpx;padding: 20rpx;">推荐</text>
					</view>
					<view class='scroll-item'>
						<text style="font-size: 40rpx;padding: 20rpx;">附近</text>
					</view>
				</view>
			</scroll-view>
			<view slot="right" >
				<uni-icons type="plus" size="24"></uni-icons>
			</view>
		</uni-nav-bar>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				 scrollIntoIndex: '0',
			}
		},
		methods: {

		}
	}
</script>


<style>
	.scroll-item{
		/* display: inline-block; */
		padding-top: 20rpx;
	}
</style>