<template>
	<view>
		<div class="main">
			<div class="underline bg-cyan radius light">
				<uni-icons type="smallcircle" size="24" color="red"></uni-icons>
				<input class="cont_input" type="text" placeholder="词条标题">
			</div>
			<div class="underline bg-cyan radius light">
				<textarea class="text_input" maxlength="256" placeholder="词条内容,长度不超过256个字!"/>
				<tm-upload></tm-upload>
			</div>
			<view class="padding flex flex-direction">
				<button class="cu-btn bg-green margin-tb-sm lg">发布</button>
			</view>
		</div>
	</view>
</template>

<script>
	import {
		uniIcons 
	} from '@dcloudio/uni-ui';
	import tmUpload from '../components/tm-upload.vue'
	export default {
		data() {
			return {
				
			}
		},
		components: {
			uniIcons,
			tmUpload
		},
		methods: {
			
		}
	}
</script>

<style scoped lang="scss">
	.main {
		
		.underline{
			border-bottom: 1px solid #ccc;
			padding: 20rpx;
			
			.cont_input {
				display: inline-block;
				line-height: 48rpx;
				width: 80%;
				padding-left: 20rpx;
			}
			
			.text_input{
				height: 400rpx;
			}
			
			.photo{
				width: 200rpx;
				height: 200rpx;
				border-radius: 10rpx;
				border: 1px solid #ccc;
			}
		}
	}
</style>
