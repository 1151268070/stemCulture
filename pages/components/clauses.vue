<template>
	<view class="content">
		<div class="left">
			<text>条目{{num+1}}：</text>
			<span>....xxx...</span>
		</div>
		<div class="right">
			<text>丨</text>
			<span>复制</span>
			<text>丨</text>
			<span @tap="gojump(2)">来源</span>
			<text>丨</text>
			<span>热度</span>
			<text>丨</text>
			<span>评论</span>
		</div>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			}
		},
		methods: {
			gojump(data) {
				if(data === 1) {
					return;
				} else if (data === 2) {
					uni.navigateTo({
						url: '/pages/source/source?id=1'
					})
				}
			}
		},
		props: ['num'],
	}
</script>

<style scoped lang="scss">
	.content {
		display: flex;
		width: 100%;
		padding: 30rpx 0rpx;
		justify-content: space-around;
		font-size: 28rpx;
		
		.left{
			width: 40%;
			overflow: hidden;
		}
	}
</style>
