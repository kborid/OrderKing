<template>
	<view class="container">
		<view class="intro">本项目已包含uni ui组件，无需import和注册，可直接使用。在代码区键入字母u，即可通过代码助手列出所有可用组件。光标置于组件名称处按F1，即可查看组件文档。</view>
		<uni-card :title="title" thumbnail="" extra="额外信息" note="">
			内容主体，可自定义内容及样式
		</uni-card>
		<image class="logo" src="/static/img/logo/logo.png" @click="goMain"></image>
		<uni-card title="Dcloud" mode="title" :is-shadow="true" thumbnail="https://img-cdn-qiniu.dcloud.net.cn/uniapp/images/muwu.jpg"
		 extra="技术没有上限" note="">
			那是一个秋意盎然、金风送爽的日子,我和父母一起来到了位于上师大旁的康健园.一踏进公园,一股浓郁的桂香扑鼻而来,泌人心脾,让我心旷神怡,只见一朵朵开得正烈的金色桂花,迎风而立,仿佛在向我招手.我们追着这桂香,走进了清幽的公园.
		</uni-card>
		<button type="default" @click="goLogin">登录</button>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				title: '我是第一页',
				href: 'https://uniapp.dcloud.io/component/README?id=uniui'
			}
		},
		methods: {
			goLogin() {
				uni.navigateTo({
					url: '/pages/login/login'
				});
			},

			goMain() {
				uni.switchTab({
					url: '/pages/main/tab/index'
				})
			}
		}
	}
</script>

<style lang="less">
	.container {
		padding: 20px;
		font-size: 14px;
		line-height: 24px;
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;

		.logo {
			height: 200rpx;
			width: 200rpx;
			margin-top: 200rpx;
			margin-left: auto;
			margin-right: auto;
			margin-bottom: 50rpx;
		}
	}
</style>
