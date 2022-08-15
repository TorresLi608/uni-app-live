<script>
	export default {
		onLaunch: function() {
			console.log('App Launch')
			// 兼容nvue 引入字体图标
			const domModule = weex.requireModule('dom')
			domModule.addRule('fontFace', {
				'fontFamily': "iconfont",
				'src': "url('~@/static/icon/iconfnt.ttf')"
			});
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
	@import url("static/icon/iconfont.css");
	/* #endif */
</style>
