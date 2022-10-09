<script>
	export default {
		onLaunch: function() {
			console.log('App Launch')
			// 兼容nvue 引入字体图标
			const domModule = weex.requireModule('dom')
			domModule.addRule('fontFace', {
				'fontFamily': "iconfont",
				'src': "url(\'http://at.alicdn.com/t/c/font_3588540_wy19ahyya6q.ttf?t=1662447814790\')"
				// 'src': 'url("'+"file:/" + plus.io.convertLocalFileSystemURL("_www/static/icon/iconfont.ttf")+'")'
			});
			const sysTemInfo = uni.getSystemInfoSync()
			// 监听底部中间按钮点击
			uni.onTabBarMidButtonTap(() => {
				uni.navigateTo({
					url: "/pages/create-live/create-live",
				})
			})
		},
		onShow: function() {
			console.log('App Show')
		},
		onHide: function() {
			console.log('App Hide')
		}
	}
</script>

<style>
	/*每个页面公共css */
	@import url("/common/free.css");
	@import url("/common/common.css");
	/* #ifndef APP-PLUS-NVUE */
	@import url("/static/icon/iconfont.css");
	/* #endif */
</style>
