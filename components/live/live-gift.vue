<template>
	<list class="gift-scroll-view" :show-scrollbar="false" >
		<cell class="flex align-center px-2 pt-3" insert-animation="default" delete-animation="default"
			v-for="(gift,index) in giftList" :key="index" :ref="'item'+index">
			<view class="info-left rounded-circle">
				<view class="p">
					<image class="info-avtar rounded-circle" :src="gift.avatar"></image>
				</view>
				<view class="flex-1">
					<text class="text-white font">{{gift.username}}</text>
					<text class="text-white font-sm">送{{gift.gift_name}}</text>
				</view>
				<view class="p">
					<image class="info-avtar rounded-circle" :src="gift.gift_image"></image>
				</view>
			</view>
			<text class="text-warning font-lg ml-1">x{{gift.num}}</text>

		</cell>
	</list>
</template>

<script>
	const dom = weex.requireModule('dom')
	export default {
		name: "live-gift",
		data() {
			return {
				giftList: []
			};
		},
		methods: {
			// 发送礼物
			send(gift){
				this.giftList.push(gift)
				this.toBottom()
				this.autoHide()
			},
			// 置于底部
			toBottom() {
				this.$nextTick(() => {
					let index = this.giftList.length - 1
					let ref = 'item' + index
					if (this.$refs[ref]) {
						dom.scrollToElement(this.$refs[ref][0], {})
					}
				})
			},
			// 自动消失
			autoHide() {
				if (this.giftList.length) {
					let timer = setTimeout(() => {
						this.giftList.splice(0, 1)
					}, 5000)
				}
			}
		}
	}
</script>

<style lang="scss" scoped>
	.gift-scroll-view {
		width: 520rpx;
		height: 500rpx;

		.info-avtar {
			width: 75rpx;
			height: 75rpx;
		}

		.info-left {
			width: 350rpx;
			display: flex;
			flex-direction: row;
			justify-content: space-between;
			align-items: center;
			background-image: linear-gradient(to right, #BCABB1, #65AAF0);
		}
	}
</style>
