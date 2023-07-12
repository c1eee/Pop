<template>
	<view>
		<swiper style="height: 100vh;" vertical="true">
			<swiper-item v-for="(item,index) in 6">
				<swiper class="pic">
					<swiper-item v-for="(item,index) in 6">
						<image class="pic-image" src="../../static/微信图片_20230712154913.jpg" mode="scaleToFill"></image>
					</swiper-item>
				</swiper>
				<!-- <view class="pic">
					<image class="pic-image" src="../../static/logo.png" mode="scaleToFill"></image>
				</view> -->
				<view class="content">
					<h1 style="padding-left: 30rpx;">老头乐</h1>
					<h4 style="padding-left: 40rpx;padding-right: 40rpx;">
					乐乐乐乐乐乐乐乐乐乐乐乐乐乐乐乐乐乐乐乐乐乐乐乐乐乐乐乐乐乐
					</h4>
				</view>
				<view class="icon">
					<uni-icons type="checkmarkempty" size="70"></uni-icons>
					<uni-icons type="heart" size="70"></uni-icons>
					<uni-icons type="chatbubble" size="70"></uni-icons>
					<uni-icons type="close" size="70"></uni-icons>
				</view>
			</swiper-item>
		</swiper>
	</view>
</template>

<script>
</script>

<style>
	.pic {
		height: 40%;
		display: flex;
		justify-content: center;
		align-items: center;
		border-radius: 30rpx;
/* 		border: 1rpx solid #000000; */
		margin: 30rpx;
	}
	.pic-image {
		width: 100%;
		height: 100%;
		border-radius: 30rpx;
	}
	.content{
		height: 25%;
		/* border: 1rpx solid #000000; */
		border-radius: 30rpx;
		margin: 30rpx;
	}
	.icon{
		height: 15%;
		/* border: 1rpx solid #000000; */
		border-radius: 30rpx;
		margin: 30rpx;
	}
</style>