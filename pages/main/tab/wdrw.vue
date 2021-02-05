<template>
	<view class="content">
		<uni-list>
		    <uni-list-item :show-extra-icon="true" :extraIcon="extraIconData" title="帐号管理" ></uni-list-item>
			<uni-list-item :show-extra-icon="true" :extraIcon="extraIconData" title="新消息通知" ></uni-list-item>
			<uni-list-item :show-extra-icon="true" :extraIcon="extraIconData" title="帮助与反馈" ></uni-list-item>
			<uni-list-item :show-extra-icon="true" :extraIcon="extraIconData" title="服务条款及隐私" ></uni-list-item>
			<uni-list-item :show-extra-icon="false" :extraIcon="extraIconData" title="关于应用" ></uni-list-item>
		</uni-list>
		<uni-list v-for="(item, index) in data">
			
			<uni-list-item title="列表左侧带略缩图" note="列表描述信息" thumb="/static/img/logo/logo.png" rightText="右侧文字"></uni-list-item>
		</uni-list>
		<!-- 单行内容显示 -->
		<!-- <uni-list>
		    <uni-list-item  title="列表文字" ></uni-list-item>
		    <uni-list-item :disabled="true" title="列表禁用状态" ></uni-list-item>
		</uni-list> -->
		<!-- 多行内容显示 -->
		<!-- <uni-list>
		    <uni-list-item title="列表文字" note="列表描述信息"></uni-list-item>
		    <uni-list-item :disabled="true" title="列表文字" note="列表禁用状态"></uni-list-item>
		</uni-list> -->
		<!-- 右侧显示角标、switch -->
		<!-- <uni-list>
		    <uni-list-item  title="列表右侧显示角标" :show-badge="true" badge-text="12" ></uni-list-item>
		    <uni-list-item title="列表右侧显示 switch"  :show-switch="true"  @switchChange="switchChange" ></uni-list-item>
		</uni-list> -->
		 <!-- 左侧显示略缩图、图标 -->
		<!-- <uni-list>
		    <uni-list-item title="列表左侧带略缩图" note="列表描述信息" thumb="/static/img/logo/logo.png" rightText="右侧文字"></uni-list-item>
		    <uni-list-item :show-extra-icon="true" :extraIcon="extraIconData" title="列表左侧带扩展图标" ></uni-list-item>
		</uni-list> -->
		<uni-list v-for="(item, index) in data">
			<uni-list-item :title="item.title" :note="item.desc" thumb="/static/img/logo/logo.png" :rightText="price(item)"></uni-list-item>
		</uni-list>
	</view>
</template>

<script>
	export default {
		name:'wdrw',
		data() {
			return {
				title: '我的任务',
				extraIconData: {
					type: 'weixin',
					color: '#FF0000',
					size: 20
				},
				data:[
					{
						title: '刷单任务',
						desc: '清空购物车',
						price:1.75
					},
					{
						title: '刷单任务',
						desc: '收藏+好评',
						price: 2.00
					},
					{
						title: '刷单任务',
						desc: '清空购物车',
						price:1.75
					},
					{
						title: '刷单任务',
						desc: '收藏+好评',
						price: 2.00
					},
					{
						title: '刷单任务',
						desc: '清空购物车',
						price:1.75
					},
					{
						title: '刷单任务',
						desc: '收藏+好评',
						price: 2.00
					},
					{
						title: '刷单任务',
						desc: '清空购物车',
						price:1.75
					},
					{
						title: '刷单任务',
						desc: '收藏+好评',
						price: 2.00
					},
					{
						title: '刷单任务',
						desc: '清空购物车',
						price:1.75
					},
					{
						title: '刷单任务',
						desc: '收藏+好评',
						price: 2.00
					},
					{
						title: '刷单任务',
						desc: '清空购物车',
						price:1.75
					},
					{
						title: '刷单任务333',
						desc: '收藏+好评',
						price: 2.00
					}
				]
			}
		},
		onLoad() {
		},
		methods: {
			switchChange(value) {
				console.log('switchChange', value);
			}
		},
		computed: {
			price() {
				return function(item) {
					return `奖励：¥${item.price}元`;
				}
			}
		}
	}
</script>

<style lang="less">
	.content {
	}
</style>
