<template>
	<view class="content">
		<taskInfo @goPersonInfo='goPersonInfo'></taskInfo>
	</view>
</template>

<script>
	import taskInfo from "../../components/taskInfo.vue";
	export default {
		components:{
			taskInfo
		},
		data() {
			return {
				title: 'Hello'
			}
		},
		onLoad() {
		
		},
		methods: {
			goPersonInfo () {
				console.log('点击进入个人中心')
				uni.navigateTo({
				    url: '/pages/personInfo/personInfo'
				})
			}
		}
	}
</script>

<style>
	.content {
	  background: url('../../static/images/taskInstrBg.png') no-repeat;
	  width: 100%;
	  height: 100%;
	  min-height: 100vh;
	  overflow: hidden;
	  background-size: 100%;
	  padding-bottom: 50px;
	  position: relative;
	}

	.logo {
		height: 200upx;
		width: 200upx;
		margin-top: 200upx;
	}

	.title {
		font-size: 36upx;
		color: #8f8f94;
	}
</style>
