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
	    		<view style="display: flex ;justify-content: space-between;padding: 40rpx 80rpx 25rpx 50rpx;">
	    			<view>
	    				<u-circle-progress active-color="#2C5DFE" inactive-color="#FF9500"  :percent="part" >
	    						<view class="u-progress-content">
	    							<text class='u-progress-info'>做题统计</text>
	    						</view>
								
	    					</u-circle-progress>
	    			</view>
					<view class="middle_text">
						<view class="middle_title">
							做题进度
						</view>
						<view class="line_1" style="display: flex;margin-top: 20rpx;">
							<view class="box_1">
								<view class="box_2"></view>
							</view>
							<view>
								总题数1300
							</view>
						</view>
						<view class="line_1" style="display: flex;margin-top: 20rpx;">
							<view class="box_1">
								<view class="box_2"></view>
							</view>
							<view>
								总题数1300
							</view>
						</view>
						<view class="line_1" style="display: flex;margin-top: 20rpx;">
							<view class="box_1">
								<view class="box_2"></view>
							</view>
							<view>
								总题数1300
							</view>
						</view>
					</view>
	    		</view>
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
				part:50
			}
		},
		methods: {
			
		}
	}
</script>

<style>
	.box_2{
		width: 20rpx;
		height: 20rpx;
		margin-left: 5rpx;
		margin-top: 5rpx;
		background-color: white;
	}
	.box_1{
		width: 30rpx;
		height: 30rpx;
		/* line-height: 40rpx; */
		border-radius:3rpx ;
		background-color: #0CAF00;
		margin-right: 10rpx;
	}
	.circulal{
		width: 225rpx;
		height: 225rpx;
		line-height: 225rpx;
		border-radius: 50%;
		background-color: #000000;
		color:white;
		text-align: center;
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
	.middle_1{
		width: 90%;
		height: 300rpx;
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
