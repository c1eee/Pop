<template>
	<view class="container">
		<view class="viewbox">
			<view class="nightmodel">
				<text class="label">黑夜模式</text>
				<switch checked="true" @change="" />
			</view>
		</view>

		<view class="viewbox">
			<view class="bigword">
				<text class="label">大字模式</text>
				<switch checked="true" @change="" />
			</view>
		</view>

		<view class="viewbox">
			<view class="light">
				<view class="title">
					<text>亮度调节</text>
				</view>
				<view class="slider-container">
					<slider class="brightness-slider" :value="brightnessValue" max="100" @change="changeBrightness">
					</slider>
				</view>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {

			return {
				brightnessValue: 50 // 初始化亮度值
			}
		},
		methods: {
			changeBrightness(event) {
				const brightness = event.mp.detail.value / 100 // 将滑块的值转换为亮度范围（0-1）
				uni.setScreenBrightness({
					value: brightness,
					success: () => {
						console.log('亮度设置成功')
					},
					fail: (error) => {
						console.log('亮度设置失败', error)
					}
				})
			},
			updateBrightness() {
				uni.getScreenBrightness({
					success: (res) => {
						const brightness = res.value * 100 // 将亮度范围（0-1）转换为滑块的值
						this.brightnessValue = brightness
					},
					fail: (error) => {
						console.log('获取亮度失败', error)
					}
				})
			}
		},
		mounted() {
			this.updateBrightness() // 获取初始亮度值
		}
	}
</script>

<style>
	.container {
		margin: 20px;
	}

	.viewbox {
		margin-bottom: 20px;
	}

	.nightmodel,
	.bigword {
		display: flex;
		justify-content: space-between;
		align-items: center;
		padding: 10px;
		background-color: #f5f5f5;
		border-radius: 5px;
	}

	.light {
		background-color: #f5f5f5;
		padding: 10px;
		border-radius: 5px;
	}

	.title {
		text-align: center;
		margin-top: 20px;
	}

	.slider-container {
		margin: 20px;
	}

	.brightness-slider {
		width: 100%;
	}
</style>