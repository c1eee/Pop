<template>
	<view class="container">
		<view class="section">
			<view class="title">基本信息</view>
			<view class="viewbox" @click="gtname">
				<view class="label">我的姓名</view>
				<view class="data">
					<text>姓名数据</text>
				</view>
			</view>
			<view class="viewbox" @click="gtemail">
				<view class="label">我的邮箱</view>
				<view class="data">
					<text>邮箱数据</text>
				</view>
			</view>
			<view class="viewbox" @click="gtphone">
				<view class="label">我的电话</view>
				<view class="data">
					<text>电话数据</text>
				</view>
			</view>
		</view>

		<view class="section">
			<view class="title">设置选项</view>
			<view class="viewbox" @click="gtmessage">
				<text>消息设置</text>
			</view>
			<view class="viewbox" @click="gtAcc">
				<text>辅助功能</text>
			</view>
			<view class="viewbox" @click="gtpersonal">
				<text>个性化设置</text>
			</view>
		</view>

		<view class="section">
			<view class="title">其他选项</view>
			<view class="viewbox" @click="gtPA">
				<text>隐私协议</text>
			</view>
			<view class="viewbox" @click="gtid">
				<text>实名认证</text>
			</view>
			<view class="viewbox" @click="gtfk">
				<text>客服反馈</text>
			</view>
		</view>

		<view class="section">
			<view class="bottom">
				<button class="exit" @click="out">退出登录</button>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {

			}
		},
		methods: {
			out() {

			},
			/* 跳转页面 */
			gtAcc() {
				uni.navigateTo({
					url: "/pages/set view/Accessibility/Accessibility"
				})
			},
			gtpersonal() {
				uni.navigateTo({
					url: "/pages/set view/Personalization/Personalization"
				})
			},
			gtmessage() {
				uni.navigateTo({
					url: "/pages/set view/message set/message set"
				})
			},
			gtname() {
				uni.navigateTo({
					url: "/pages/set view/name/name"
				})
			},
			gtphone() {
				uni.navigateTo({
					url: "/pages/set view/phone/phone"
				})
			},
			gtemail() {
				uni.navigateTo({
					url: "/pages/set view/email/email"
				})
			},
			gtid() {
				uni.navigateTo({
					url: "/pages/set view/id/id"
				})
			},
			gtPA() {
				uni.navigateTo({
					url: "/pages/set view/Privacy Agreement/Privacy Agreement"
				})
			},
			gtfk() {
				uni.navigateTo({
					url: "/pages/set view/kefu/kefu"
				})
			}
		},

	}
</script>

<style>
	.container {
		display: flex;
		flex-direction: column;
		align-items: center;
		margin: 20px;
	}

	.section {
		width: 100%;
		margin-bottom: 20px;
	}

	.title {
		font-size: 18px;
		font-weight: bold;
		margin-bottom: 10px;
	}

	.viewbox {
		display: flex;
		justify-content: space-between;
		align-items: center;
		padding: 10px;
		background-color: #f5f5f5;
		border-radius: 5px;

	}

	.label {
		font-weight: bold;
	}

	.data {
		color: #666666;
	}

	.bottom {
		display: flex;
		justify-content: center;
		margin-top: 20px;
	}

	.exit {
		padding: 10px 20px;
		background-color: gray;
		color: #ffffff;
		border: none;
		border-radius: 5px;
		font-weight: bold;
	}
</style>