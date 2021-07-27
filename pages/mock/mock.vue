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
	    	<view class="row">
	    		<view class="row_1">
	    			考试车型
	    		</view>
	    		<view class="row_2">
	    			<view style="margin-left: 20rpx;">汽车C1/C2/C3</view>
	    		</view>
	    	</view>
	    	<view class="row">
	    		<view class="row_1">
	    			考试车型
	    		</view>
	    		<view class="row_2">
	    			<view style="margin-left: 20rpx;">汽车C1/C2/C3</view>
	    		</view>
	    	</view>
	    	<view class="row">
	    		<view class="row_1">
	    			考试车型
	    		</view>
	    		<view class="row_2">
	    			<view style="margin-left: 20rpx;">汽车C1/C2/C3</view>
	    		</view>
	    	</view>
	    	<view class="row">
	    		<view class="row_1">
	    			考试车型
	    		</view>
	    		<view class="row_2">
	    			<view style="margin-left: 20rpx;">汽车C1/C2/C3</view>
	    		</view>
	    	</view>
	    </view>
		<view class="middle2">
			<navigator url="../library/library">
				<view class="test1">
					模拟考试
				</view>
			</navigator>
			<view class="test2">
				考场模拟
			</view>
	    </view>
	    <view class="footer">
	    	<view class="footer_1">
	    		评分规则:模拟考试不能修改答案，每错1题扣1分，错题累计超过10道，考试不通过，系统自动提醒交卷。
	    	</view>
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
	.footer_1{
		padding:30rpx 30rpx 10rpx 30rpx;
	}
	.footer{
		width: 80%;
		height: 180rpx;
		background-color:#EAEFFF;
		 margin-left: 10%;
		 margin-top: 80rpx;
		 border-radius:10rpx;
		 font-size: 28rpx;
	}
	.test2{
		width: 60%;
		height: 80rpx;
		line-height: 80rpx;
		border-radius: 20rpx;
		color: #2C5DFE;
		font-size: 35rpx;
		text-align: center;
		margin-left: 20%;
		margin-top: 50rpx;
		border: 1rpx solid #2C5DFE;
		
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
	.row_2{
		width: 425rpx;
		height:80rpx ;
		line-height: 80rpx;
		border-radius:20rpx ;
		background-color: #F1F1F1;
		margin-left: 30rpx;
	}
	.row_1{
		width: 200rpx;
		height: 80rpx;
		line-height: 80rpx;
		background-color: #2C5DFE;
		border-radius: 20rpx;
		color: white;
		text-align: center;
	}
	.row{
		font-size: 35rpx;
		display: flex;
		margin-left: 40rpx;
		margin-top: 50rpx;
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
