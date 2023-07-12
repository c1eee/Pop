<template>
	<view>
		<indexdaohanglan></indexdaohanglan>
		<card></card>
	</view>
		<!-- 内容 -->
		<!-- <view class="content">
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
		</view> -->
	</view>
</template>

<script>
	import card from "../../components/index/card.vue"
	import indexdaohanglan from "../../components/index/indexdaohanglan.vue"
	export default {
	components:{
		indexdaohanglan,
		card
	}
	};
</script>


<style>
	
</style>