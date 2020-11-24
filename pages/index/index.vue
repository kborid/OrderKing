<template>
	<view class="container">
		<view class="intro">本项目已包含uni ui组件，无需import和注册，可直接使用。在代码区键入字母u，即可通过代码助手列出所有可用组件。光标置于组件名称处按F1，即可查看组件文档。</view>
		<uni-card title="标题文字" thumbnail="" extra="额外信息" note="">
			内容主体，可自定义内容及样式
		</uni-card>
		<uni-calendar style="margin:50rpx 0;" lunar="" @change=""></uni-calendar>
		<button type="default" @click="clickMe">点击我</button>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				href: 'https://uniapp.dcloud.io/component/README?id=uniui'
			}
		},
		methods: {
			clickMe() {
				uni.showToast({
					title: '你点了我'
				});
			}
		}
	}
</script>

<style>
	.container {
		padding: 20px;
		font-size: 14px;
		line-height: 24px;
	}
</style>
