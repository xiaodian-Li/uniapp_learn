<template>
	 <view>
	        <view class="uni-padding-wrap uni-common-mt">
	            <view class="uni-title uni-common-mt">
	                flex-direction: row
	                <text>\n横向布局</text>
	            </view>
	            <view class="uni-flex uni-row">
	                <view class="flex-item uni-bg-red">A</view>
	                <view class="flex-item uni-bg-green">B</view>
	                <view class="flex-item uni-bg-blue">C</view>
	            </view>
	            <view class="uni-title uni-common-mt">
	                flex-direction: column
	                <text>\n纵向布局</text>
	            </view>
	            <view class="uni-flex uni-column">
	                <view class="flex-item flex-item-V uni-bg-red">A</view>
	                <view class="flex-item flex-item-V uni-bg-green">B</view>
	                <view class="flex-item flex-item-V uni-bg-blue">C</view>
	            </view>
	        </view>
	    </view>
</template>

<script>
	export default {
		data() {
			return {
				title: 'Hello'
			}
		},
		onLoad() {

		},
		methods: {

		}
	}
</script>

<style>
	.uni-flex {
		display: flex;
	}
	.uni-row {
		flex-direction: row;
	}
	.uni-column {
		flex-direction: column;
	}
	.flex-item {
		width: 33.3%;
		height: 200upx;
		text-align: center;
		line-height: 200upx;
		color: #ffffff;
	}
	.uni-bg-red {
		background: #2C405A;
	}
	.uni-bg-green {
		background: #3F536E;
	}
	.uni-bg-blue {
		background: #808080;
	}
</style>
