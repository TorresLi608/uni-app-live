<template>
	<view class="">
		<view class="flex align-center">
			<view class="flex align-center justify-center"
			style="width: 180rpx;height: 181rpx;">
				<image src="/static/gift/1.png" class="rounded-circle"  style="width: 105rpx;height: 105rpx;" mode=""></image>
			</view>
			<view class="flex flex-column">
				<text class="font-md">昵称</text>
				<text class="font text-muted">描述</text>
			</view>
			<view class="ml-auto mr-3" hover-class="bg-light">
				<view class="border border-main rounded flex align-center justify-center p-2">
					<text class="text-main font">编辑资料</text>
				</view>
			</view>
		</view>
		<view class="f-divider"></view>
		<f-list-item title="我的金币" icon="icon-liwu" :showRight="false">
			<text class="text-muted font">50金币 立即充值</text>
		</f-list-item>
		<f-list-item title="我的直播" icon="icon-liwu" >
			<text class="text-muted font">0</text>
		</f-list-item>
		<f-list-item title="我的关注" icon="icon-liwu" >
			<text class="text-muted font">0</text>
		</f-list-item>
		<f-list-item title="历史记录" icon="icon-liwu" >
		</f-list-item>
	</view>
</template>
<script>
	import FListItem from '../../components/common/f-list-item.vue'
	export default {
		components:{FListItem,},
		data() {
			return {
				title: "title"
			}
		}
	}
</script>
<style>

</style>
