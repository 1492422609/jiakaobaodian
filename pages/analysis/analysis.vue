<template>
	<view>
		<view class="protect">
			<view class="bg_box">
				<view style="text-align: center;padding: 30rpx;font-size: 35rpx;">
					技巧解析
				</view>
				<view style="font-size: 30rpx;margin:20rpx;">
					超车前需从前车左侧超越，以下说法正确的是?
				</view>
				<view class="">
					<view style="display: flex;margin: 20rpx; color:green ;">
						<view>
							√
						</view>
						<view style="margin-left: 30rpx;">
							我国实行左侧通行原则
						</view>
					</view>
					<view style="display: flex;margin: 20rpx;">
						<view>
							B
						</view>
						<view style="margin-left: 30rpx;">
							我国实行左侧通行原则
						</view>
					</view>
					<view style="display: flex;margin: 20rpx;">
						<view>
							C
						</view>
						<view style="margin-left: 30rpx;">
							我国实行左侧通行原则
						</view>
					</view>
					<view style="display: flex;margin: 20rpx;">
						<view>
							D
						</view>
						<view style="margin-left: 30rpx;">
							我国实行左侧通行原则
						</view>
					</view>
				</view>
			    <view style="margin:40rpx 30rpx; font-size: 35rpx;">
			    	技巧解析技巧解析技巧解析技巧解析技巧解析技巧解析技巧解析技巧解析
			    </view>
				<view class="box_bottom">
					<view class="box_bottom">
						<view class="box_bottom_left">
							<view style="display: flex;">
								<image src="https://z3.ax1x.com/2021/07/29/WHp9fA.png" mode="widthFix" class="box_bottom_photo"></image>
								<view class="">
									继续答题
								</view>
							</view>
						</view>
						<view class="box_bottom_left">
							<view style="display: flex;">
								<image src="https://z3.ax1x.com/2021/07/29/WHppYd.png" mode="widthFix" class="box_bottom_photo"></image>
								<view style="color: #FF0000;">
									现在交卷
								</view>
							</view>
						</view>
					</view>  
				</view>
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
	.box_bottom_photo{
		width: 45rpx;
		margin-top: 5rpx;
		margin-right: 20rpx;

	}
	.box_bottom_left{
		padding: 60rpx;
		font-size: 38rpx;
	}
	.box_bottom{
		display: flex;
	    justify-content: space-between;
		margin-top: 30rpx;
	}
	.bg_box{
		width: 90%;
		margin-left: 5%;
		margin-top: 200rpx;
		height: 750rpx;
		border-radius: 30rpx;
		background-color: white;
	}
	.protect{
			width:100% ;
			height: 1250rpx;
			background:rgba(0, 0, 0, 0.4);
			position:absolute;
			z-index: 10;
			/* margin-top: -1500rpx; */
			overflow: hidden;
	}
</style>
