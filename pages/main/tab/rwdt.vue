<template>
	<view>
		<uni-card @click="clickCard">这是一个基础卡片示例，内容较少，此示例不带边框阴影。</uni-card>
	</view>
</template>

<script>
	export default {
		name: 'rwdt',
		components: {},
		data() {
			return {
				title: '任务大厅'
			}
		},
		onLoad() {},
		methods: {
			onNavigationBarButtonTap(e) {
				uni.showToast({
					title: '导航栏按钮被点击'
				});
			},
			
			clickCard() {
				uni.showToast({
					title: 'card被点击'
				});
			}
		}
	}
</script>

<style lang="less">
</style>
