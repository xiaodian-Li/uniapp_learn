<template>
	<view>
	<view class="task-instr">
	  <view class="left">
		<view class="circle"></view>
		<view class="vLine"></view>
		<view class="circle"></view>
		<view class="vLine"></view>
		<view class="circle"></view>
	  </view>
	  <view class="right">
		<view class="base">
		  <view class="base-crash">
			<view class="base-reward">88元</view>
			<text class="base-text">现金</text>
		  </view>
		  <view class="cuting"></view>
		  <view class="base-order">
			<text class="base-finish">完成<span>88单</span></text>
			<text class="base-money">即可获得<span>88元</span></text>
		  </view>
		</view>
		<view class="add">
		  <view class="add-crash">
			<view class="add-reward">无上限</view>
			<text class="add-text">现金</text>
		  </view>
		  <view class="cuting add-cuting"></view>
		  <view class="add-order">
			<text class="add-finish">完成<span class="finsh-order">88单</span>及以上</text>
			<text class="add-money">每多<span class="finsh-order">1单</span>，再加<span class="finsh-money">88元</span></text>
		  </view>

		</view>
		<view class="mark">完单越多，奖励越多，最高奖励无上限！</view>
	  </view>
	</view>
	<view class="task-btn">
	  <view class="cancel-btn" @tap='onCancel'>暂不考虑</view>
	  <view class="confirm-btn" @tap='onConfirm'>领取任务</view>
	</view>
	</view>
</template>

<script>
	export default {
		name: "taskInfo",
		data() {
			return {
				
			};
		},
		methods: {
			onCancel () {
				this.$emit('onCancle')
			},
			onConfirm () {
				this.$emit('goPersonInfo')
			}
		}
	}
</script>

<style>
.task-instr {
  margin: 337px auto 0;
  background: url('../static/images/rewardInstr.png') no-repeat;
  width: 350px;
  height: 299.5px;
  overflow: hidden;
  background-size: cover;
  display: flex;
}
.left {
  margin-left: 26px;
  margin-top: 55px;
}
.circle {
	width: 7.5px;
	height: 8px;
	border-radius: 50%;
	background-color:rgb(176, 108, 19);
}
.vLine {
	border-left: dotted 2px rgb(176, 108, 19);
	height: 95px;
	vertical-align: middle;
	display: inline-block;
}
.base, .add{
  margin-left: 11.5px;
  display: flex;
  width: 268px;
  height: 89px;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}
.base-crash {
	margin: 0 10.5px 0 -10.5px;
}
.add-crash {
	margin: 0 16px 0 16px;
}
.base-reward, .add-reward {
	margin-top: 8px;
	font-size: 15px;
	font-family: PingFangSC-Medium;
	color: #fff;
}
.add-reward {
	font-size: 15px;
	color: rgb(176, 108, 19);
	width: 49px;
}
.base-text, .add-text {
	margin: auto;
	margin-top: 8px;
	border-radius: 12.5px;
	width: 41px;
	height: 16px;
	line-height: 16px;
	font-size: 10px;
	font-family: PingFangSC-Medium;
	}
.base-text {
	color: rgb(255, 162, 170);
	background: rgb(245, 50, 72);
}
.add-text {
	color: rgb(176, 108, 19);
	background: rgb(237, 198, 138);
}
.base-order, .add-order {
	margin: 15px 0 0 16.5px;
	font-size: 16px;
	font-family: PingFangSC-Regular;
	text-align: left;
	color: #fff;
}
span {
	color: rgb(255, 240, 0);
}
.add-order {
	color:rgb(176, 108, 19);
}
.finsh-order, .finsh-money {
	color:rgb(227, 16, 39);
}
.base-money, .add-money {
	margin-top: 6.5px;
}
.cuting {
  margin-top: 15px;
  border-left: dotted 2px #fff;
  height: 37.5px;
  vertical-align: middle;
  display: inline-block;
}
.add-cuting {
  border-left: dotted 2px rgb(176, 108, 19);
}
.base {
  margin-top: 50px;
  background: url('../static/images/basicReward.png') no-repeat;
  background-size: 100%;
}
.add {
  margin-top: 16px;
  background: url('../static/images/supeReward.png') no-repeat;
  background-size: 100%;
}
.mark {
  font-family: PingFangSC-Regular;
  text-align: left;
  margin: 15px 0 0 19.5px;
  font-size: 10px;
  color: rgb(176, 108, 19);
}
.task-btn {
  display: flex;
  flex-direction: row;
  position: fixed;
  bottom: 0;
  text-align: center;
}
.cancel-btn, .confirm-btn {
    font-family: PingFangSC-Regular;
    width: 187.5px;
    line-height: 50px;
  }
  .cancel-btn {
    background: url('../static/images/yellowBtn.png') no-repeat;
    color: rgb(188, 129, 54)
  }
  .confirm-btn {
    background: url('../static/images/redBtn.png') no-repeat;
    color: #fff;
  }
</style>
