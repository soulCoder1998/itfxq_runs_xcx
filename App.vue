<script>
	export default {
		onLaunch: function() {
			console.log('App Launch')
		},
		onShow: function() {
			let username = uni.getStorageSync('loginUserName')
			
			if(!username || username==''){
				
				uni.navigateTo({
					url:'/pages/login/login'
				})
			}
		},
		onHide: function() {
			console.log('App Hide')
		},
		onError: function(){
			console.log('应用出错')
		}
	}
</script>

<style lang="scss">
	@import "uview-ui/index.scss";
	/*每个页面公共css */
	.page{
		width:100%;
		height: 100%;
		background-image: url(static/bg.jpg);
	}
	
</style>