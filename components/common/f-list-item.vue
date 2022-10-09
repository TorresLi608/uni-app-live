<template>
	<view class="p-3 flex align-center" hover-class="bg-light">
		<text class="iconfont mr-3" :class="icon"></text>
		<text class="font-md">{{title}}</text>
		<view class="ml-auto flex align-center">
			<slot></slot>
			<text v-if="showRight" class="text-main font ml-1">></text>
			
		</view>
	</view>
</template>

<script>
	export default {
		name:"f-list-item",
		props:{
			icon:{
				type:String,
				default:"",
			},
			title:{
				type:String,
				default:"",
			},
			showRight:{
				type:Boolean,
				default:true
			}
		}
	}
</script>

<style>
</style>