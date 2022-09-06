<template>
	<view class="pages-index">
		<swiper :indicator-dots="true" :autoplay="true" :interval="3000" :duration="200" class="swiper">
			<swiper-item>
				<image src="/static/image/banner/1.jpg" class="swiper-image"></image>
			</swiper-item>
			<swiper-item>
				<image src="/static/image/banner/2.jpg" class="swiper-image"></image>
			</swiper-item>
		</swiper>
		<view class="flex flex-wrap">
			<view class="live-item" v-for="item in 10" :key="item" @click="handleOpenLive">
				<image src="/static/image/1.jpg" mode="" class="live-image rounded" mode="aspectFill"></image>
				<view class="live-item-top-left rounded-circle px-2 py-1 flex align-center font-sm text-white">
					<text class="iconfont icon-jinbi icon-size text-warning mr-1"></text>0
				</view>
				<view class="live-item-top-right rounded-circle px-2 py-1 flex align-center font-sm text-white">
					人气:1
				</view>
				<view class="live-item-bottom-left rounded-circle px-2 py-1 flex align-center font-sm text-white">
					直播间
				</view>
				<view class="live-item-bottom-right rounded-circle px-2 py-1 flex align-center font-sm text-white">
					已结束
				</view>
			</view>
		</view>
	</view>
</template>
<script>
	export default {
		data() {
			return {
				title: "title"
			}
		},
		methods:{
			handleOpenLive(){
				uni.navigateTo({
					url:'/pages/live/live'
				})
			}
		}
	}
</script>
<style lang="scss" scoped>
	.pages-index {
		.swiper {
			width: 100%;
			height: 250rpx;
		}

		.swiper-image {
			width: 100%;
			height: 250rpx;
		}
	}

	.live-item {
		width: 375rpx;
		height: 375rpx;
		padding: 5rpx;
		box-sizing: border-box;
		position: relative;

		// .icon-size {
		// 	font-size: 13px;
		// }

		.live-image {
			width: 365rpx;
			height: 365rpx;
		}

		.live-item-top-left {
			position: absolute;
			left: 15rpx;
			top: 15rpx;
			background-color: rgba(0, 0, 0, 0.4);
		}

		.live-item-top-right {
			position: absolute;
			right: 15rpx;
			top: 15rpx;
			background-color: rgba(0, 0, 0, 0.4);
		}

		.live-item-bottom-left {
			position: absolute;
			left: 15rpx;
			bottom: 15rpx;
			// background-color: rgba(0,0,0,0.4);
		}

		.live-item-bottom-right {
			position: absolute;
			right: 15rpx;
			bottom: 15rpx;
			background-color: rgba(0, 0, 0, 0.4);
		}
	}
</style>
