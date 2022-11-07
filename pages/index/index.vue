<template>
	<view>
		<u-action-sheet :list="list"></u-action-sheet>
		<u-icon label="uView" size="40" name="https://cdn.uviewui.com/uview/example/button.png"></u-icon>
		<view class="u-page">
			<u-action-sheet :actions="list" :title="title" :show="show"></u-action-sheet>
			<u-button @click="show = true">打开ActionSheet</u-button>
		</view>
		</view>
</template>

<script>
	export default {
		data() {
			return {
			title:'标题',
			list: [
				{
					name:'选项一',
					subname:"选项一描述",
					color:'#ffaa7f',
					fontSize:'20'
				},
				{
					name: '选项二禁用',
					disabled:true
				},
				{
					name: '开启load加载', //开启后文字不显示
					loading:true
				}
			],
			show: false,
			}
		},

	}
</script>

<style lang="scss">
	.wrap {
		padding: 12px;
	}

	.demo-layout {
		height: 25px;
		border-radius: 4px;
	}

	.bg-purple {
		background: #CED7E1;
	}

	.bg-purple-light {
		background: #e5e9f2;
	}

	.bg-purple-dark {
		background: #99a9bf;
	}

	.content {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
	}

	.logo {
		height: 200rpx;
		width: 200rpx;
		margin-top: 200rpx;
		margin-left: auto;
		margin-right: auto;
		margin-bottom: 50rpx;
	}

	.text-area {
		display: flex;
		justify-content: center;
	}

	.title {
		font-size: 36rpx;
		color: #8f8f94;
	}
</style>
