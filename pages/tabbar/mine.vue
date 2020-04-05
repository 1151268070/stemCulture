<template>
	<view class="bg-gradual-purple padding radius text-center shadow-blur">
		<view class="padding" style="text-align: center;">
			<view class="cu-avatar xl round margin-left" style="background-image:url(https://ossweb-img.qq.com/images/lol/web201310/skin/big99008.jpg);"></view>
		</view>
		<view class="text-center text-blue" style="font-size: 32rpx;">用户名</view>
		<view class="uni-top cu-list menu card-menu">
			<view class="cu-item arrow">
				<view class="content">
					<text class="cuIcon-write text-grey"></text>
					<text class="text-grey">我发布的词条</text>
				</view>
			</view>
			<view class="cu-item arrow">
				<view class="content">
					<text class="cuIcon-hot text-grey"></text>
					<text class="text-grey">我点赞的词条</text>
				</view>
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

		}
	}
</script>

<style scoped lang="scss">
	.uni-top {
		margin-top: 50rpx;
	}
</style>
