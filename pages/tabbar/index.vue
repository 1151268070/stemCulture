<template>
	<view class="content">
		<div class="theme"></div>
		<div class="main">
			<div class="fixed">
				<uni-search-bar placeholder="请输入关键词" :cancelButton="none" :radius="100" @confirm="search"></uni-search-bar>
				<scroll-view class="scroll-view_H" scroll-x="true" style="width: 100%">
					<view v-for="i in 10" class="category" scroll-left="120" :key="i">类别{{i}}</view>
				</scroll-view>
				<div class="sort">
					<view class="condition">热度</view>
					<view class="condition">时间</view>
					<view class="condition">近期</view>
				</div>
			</div>
			<div class="normals bg-gradual-blue radius shadow-blur">
				<clause v-for="k in 15" :num="k" :key="k"></clause>
			</div>
		</div>
	</view>
</template>

<script>
	import clause from '../components/clauses.vue'
	import {
		uniSearchBar
	} from '@dcloudio/uni-ui';
	export default {
		data() {
			return {
				title: 'Hello',
			}
		},
		components: {
			uniSearchBar,
			clause
		},
		onLoad() {

		},
		methods: {
			search(e) {
				console.log(e)
			}
		}
	}
</script>

<style scoped lang="scss">
	.content {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;

		.main {
			width: 100%;

			.fixed {
				width: 100%;
				position: fixed;
				top: 0;
				left: 0;
				z-index: 9;
				background-color: #fff;

				.scroll-view_H {
					white-space: nowrap;
					margin: 30rpx 0;

					.category {
						width: 120rpx;
						height: 60rpx;
						background-color: red;
						display: inline-block;
						text-align: center;
						line-height: 60rpx;
						margin: 0 10rpx;
					}
				}
				
				.sort {
					width: 70%;
					height: 60rpx;
					padding-left: 20rpx;
				
					.condition {
						display: inline-block;
						border-bottom: 2rpx solid #ccc;
						width: 100rpx;
						margin-right: 10rpx;
						line-height: 60rpx;
						text-align: center;
					}
				}
			}

			.normals {
				width: 100%;
				margin-top: 290rpx;
			}
		}
	}
</style>
