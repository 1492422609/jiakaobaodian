<template>
	<view>
		<view class="header">
			<view class="avater">
				<image src="https://z3.ax1x.com/2021/07/26/WWcPET.png" mode="widthFix" style="width: 150rpx;"></image>
				<view class="name">
					芜湖起飞
				</view>
			</view>
		</view>
	    <view class="middle">
	    	<view class="middle_1">
	    		
	    	</view>
	    </view> 
		<view class="bottom">
			<navigator url="../library/library">
				<view class="test1">
					开始答题
				</view>
			</navigator>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			}
		},
		methods: {
			
		}
	}
</script>

<style>
	.test1{
		width: 60%;
		height: 85rpx;
		line-height: 80rpx;
		background-color: #2C5DFE;
		border-radius: 20rpx;
		color: white;
		font-size: 35rpx;
		text-align: center;
		margin-left: 20%;
		margin-top: 80rpx;
	}
	.middle_1{
		width: 90%;
		height: 400rpx;
		/* background-color: #0000FF; */
		margin-left: 5%;
		margin-top: 60rpx;
		border-radius: 30rpx;
		box-shadow: 1px 1px 2px 2px rgba(0, 0, 0, 0.1);
	}
	.name{
		font-size: 38rpx;
		margin-top: 10rpx;
	}
	.avater{
		text-align: center;
	    margin-top: 40rpx; 
	}
</style>
