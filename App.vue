<script>
	export default {
		onLaunch: function() {
			console.log('App Launch')
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
  
  @import “/wxcomponents/vant/common/index.wxss”;
  /* 定义 sidebar的宽度 */
  :root {
    --sidebar-width:30vw;
  }
  
  *{
    margin: 0;
    padding: 0;
  }
  
</style>
