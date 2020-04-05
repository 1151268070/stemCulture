<template>
	<view>
		<text>梗文化</text>
		<view class='titleText'>申请获取以下权限</view>
		<view class='contentText'>获得你的公开信息(昵称,头像,手机等)</view>
		<button 
			v-if="canIUse"
			class='authBtn'
			type='primary'
			open-type='getUserInfo'
			@getuserinfo='bindGetUserInfo'>授权登录</button>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				isHide: false,
				canIUse: wx.canIUse('button.open-type.getUserInfo'),
				visibleNote: 1
			};
		},
		methods: {
			bindGetUserInfo(e) {
				console.log(e);
			}
		},
		onLoad() {
			var that = this;
			//查看是否授权
		},
	}
</script>

<style scoped lang="scss">

</style>
