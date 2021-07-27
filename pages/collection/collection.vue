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
	    		<image src="https://z3.ax1x.com/2021/07/26/WflSld.png" mode="widthFix" class="middle_photo"></image>
	    	    <view class="middle_text">
	    	    	全部错题
	    	    </view>
				<view class="middle_text2">
					50
				</view>
				<view class="middle_text3">
					道
				</view>
			</view>
	    </view> 
		<view class="bottom">
			<navigator url="../library/library">
				<view class="test1">
					全部错题
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
	.middle_text3{
		margin-left: 10rpx;
		font-size: 35rpx;
		font-weight: 600;
	}
	.middle_text2{
		margin-left: 170rpx;
		font-size: 45rpx;
		font-weight: 600;
		color:#2C5DFE ;
	}
	.middle_text{
		margin-left: 50rpx;
		font-size: 35rpx;
		font-weight: 600;
	}
	.middle_photo{
		width: 120rpx;
		margin-top: 40rpx;
		margin-left: 50rpx;
	}
	.middle_1{
		display: flex;
		width: 90%;
		height: 200rpx;
		line-height:200rpx ;
		/* background-color: #0000FF; */
		margin-left: 5%;
		margin-top: 60rpx;
		border-radius: 30rpx;
		box-shadow: 1px 1px 2px 2px rgba(0, 0, 0, 0.1);
	}
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
	
	.name{
		font-size: 38rpx;
		margin-top: 10rpx;
	}
	.avater{
		text-align: center;
	    margin-top: 40rpx; 
	}
</style>
