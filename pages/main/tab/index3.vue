<template>
	<view class="content">
		<!-- 单行内容显示 -->
		<uni-list>
		    <uni-list-item  title="列表文字" ></uni-list-item>
		    <uni-list-item :disabled="true" title="列表禁用状态" ></uni-list-item>
		</uni-list>
		<!-- 多行内容显示 -->
		<uni-list>
		    <uni-list-item title="列表文字" note="列表描述信息"></uni-list-item>
		    <uni-list-item :disabled="true" title="列表文字" note="列表禁用状态"></uni-list-item>
		</uni-list>
		<!-- 右侧显示角标、switch -->
		<uni-list>
		    <uni-list-item  title="列表右侧显示角标" :show-badge="true" badge-text="12" ></uni-list-item>
		    <uni-list-item title="列表右侧显示 switch"  :show-switch="true"  @switchChange="switchChange" ></uni-list-item>
		</uni-list>
		 <!-- 左侧显示略缩图、图标 -->
		 <uni-list>
		    <uni-list-item title="列表左侧带略缩图" note="列表描述信息" thumb="https://img-cdn-qiniu.dcloud.net.cn/new-page/uni.png"
		     thumb-size="lg" rightText="右侧文字"></uni-list-item>
		    <uni-list-item :show-extra-icon="true" extraIcon="" title="列表左侧带扩展图标" ></uni-list-item>
		</uni-list>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				title: '我的任务'
			}
		},
		onLoad() {
		},
		methods: {
			switchChange(value) {
				console.log('switchChange', value);
			}
		}
	}
</script>

<style lang="less">
	.content {
	// 	display: flex;
	// 	flex-direction: column;
	// 	align-items: center;
	// 	justify-content: center;

	// 	.text-area {
	// 		display: flex;
	// 		justify-content: center;

	// 		.title {
	// 			font-size: 36rpx;
	// 			color: #8f8f94;
	// 		}
	// 	}
	}
</style>
