<template>
	<view class="content">
		<view class="text-area">
			<text class="title">{{title}}</text>
		</view>
	</view>
</template>

<script>
	export default {
		name: 'lldrw',
		data() {
			return {
				title: '浏览单任务'
			}
		},
		onLoad() {
		},
		methods: {
		}
	}
</script>

<style lang="less">
	.content {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;

		.text-area {
			display: flex;
			justify-content: center;

			.title {
				font-size: 36rpx;
				color: #8f8f94;
			}
		}
	}
</style>
